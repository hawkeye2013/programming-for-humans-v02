---
title: 'Working With Angular and Dynamic SVGs - 1 - Component Relationships'
date: '2020-05-20T05:53:37.121Z'
template: 'post'
draft: false
slug: 'working-with-angular-and-svg-component-relationships'
category: 'Angular'
tags:
  - 'Angular'
  - 'SVG'
description: 'Set up an Angular SVG Project and Parent-Child relationships with SVGs.'
socialImage: '/media/covers/2020/working-with-angular-svg-cover.jpg'
---

![Text Edit Cover](/media/covers/2020/working-with-angular-svg-cover.jpg)

<center>Photo by Clem Onojeghuo on Unsplash</center>

## Table of Contents

**[Intro](#intro)**

**[The SVG Rendering Context](#the-svg-rendering-context)**

**[Setting up Angular](#setting-up-angular)**

**[Creating New Components](#creating-new-components)**

**[Modify SVG Parent Component](#modify-svg-parent-component)**

**[Modify SVG Child Component](#modify-svg-child-component)**

**[Adding Child to Parent](#adding-child-component-to-parent)**

## Intro

It's easy to pop an image tag into a web page and point it to an SVG file. It loads and you can resize it no problem, which is great. Sometimes that isn't enough. What happens if you want to create an interactive graph with Angular using dynamic data? That isn't just an image tag. This series will show how to use dynamic SVGs with angular components. By the end of this series, we will have a set of angular components to make a dynamic, interactive SVG plot.

## The SVG Rendering Context

Before we jump right in we should talk about SVG. SVG stands for [**S**calable **V**ector **G**raphics](https://developer.mozilla.org/en-US/docs/Web/SVG). Most pictures we see are raster graphics. Raster graphics are created from an array of pixels, each having a set of 8-bit RGB values to define the color (thus 0-255). Since there is a finite number of pixels in the array, if we zoom in far enough on the picture, we will start to see pixelation. Not awesome for high quality sites. On the other hand, SVGs are an implementation of [vector graphics](https://en.wikipedia.org/wiki/Vector_graphics). Vector graphics are defined by points, lines, and curves. Since all elements of an SVG are mathematically defined, SVGs have the ability to scale as big or small as they need to to fit the space. All elements are calculated, and therefore will not pixelate. How neat!

## Setting up Angular

We are going to start with a blank project. If you haven't already, install the Angular CLI with:

```bash
npm install -g @angular/cli
```

If you run `ng --version` it will tell you the version of angular you are using. At this time, the version I am using is:

```txt
Angular CLI: 9.1.4
Node: 12.13.1
OS: win32 x64

Angular:
...
Ivy Workspace:

Package                      Version
------------------------------------------------------
@angular-devkit/architect    0.901.4
@angular-devkit/core         9.1.4
@angular-devkit/schematics   9.1.4
@schematics/angular          9.1.4
@schematics/update           0.901.4
rxjs                         6.5.4
```

Navigate to the parent folder for your project and run:

```bash
ng new angularSVG
```

Go ahead and enter `n` for adding routing and `SCSS` for the stylesheet format. After installation, launch angular with your editor of choice and start a development server using either `npm start` or `ng serve`. If you've never used Angular before, I suggest going to check out a couple of tutorials before continuing with this series, as we will not be discussing basics.

## Creating New Components

At this point we have a fresh Angular project open. We have a development server running with live reloading. For now, let's create two components. The first will be the plot container. This component will be in charge of the SVG element. The second component will be in charge of the actual plot area. I will run

```bash
ng g component line-plot
```

and

```bash
ng g component line-plot/plot-area
```

to create these components.

## Modify SVG Parent Component

The first thing we'll do is clear out the `app.component.html` file since we don't need the boilerplate that ships with Angular. We'll then add the `LinePlotComponent` to the `AppComponent` within a `div`. I'm adding the `div` in there so we can control the parent size. I want to be able to drop this component into whatever size parent and have it resize itself. In a real application, the plot component probably wouldn't be at the top level like this and would have a parent controlling it's size, so we will build it like that. Our `app.component.html` should look like this now:

**`line-plot.component.html`**

```html
<div style="width: 800px; height: 600px">
  <app-line-plot></app-line-plot>
</div>
```

Now let's modify our line-plot template. First, we'll clear everything in the `line-plot.component.html` and add an `svg` element to the template. I'm going to set the width and height attributes of the `svg` element to `100%` and set a nice aqua background to make sure it is actually rendering to the screen.

This is what we have now in our `line-plot.component.html`.

**`line-plot.component.html`**

```html
<svg width="100%" height="100%" style="background-color: aqua;"></svg>
```

When you save, you should see an aqua square (the svg element) rendered to the page. Since the line-plot component is inheriting the size from the parent div (currently 800px by 600px) all we need to do to change the size of the svg element is to change the size of the parent `div` for the line plot.

For now, let's add a blue rectangle as a child of the `svg` element. Our `line-plot.component.html` should look like this now:

**`line-plot.component.html`**

```html
<svg width="100%" height="100%" style="background-color: aqua;">
  <rect
    width="300"
    height="100"
    style="fill: rgb(0, 0, 255); stroke-width: 3; stroke: rgb(0, 0, 0);"
  />
</svg>
```

## Modify SVG Child Component

Right now I am not worried about breaking the styles away from the template, but eventually I will be. Right now I just want to make sure I have everything rendering. If we take a look at the webpage, we should see an aqua background with a dark blue square inside. We will use this square to ensure the child component is rendering, so cut it from `line-plot.component.html` and add it to the `plot-area.component.html`. This is what our two templates look like now:

**`line-plot.component.html`**

```html
<svg width="100%" height="100%" style="background-color: aqua;"></svg>
```

**`plot-area.component.html`**

```html
<rect
  width="300"
  height="100"
  style="fill: rgb(0, 0, 255); stroke-width: 3; stroke: rgb(0, 0, 0);"
/>
```

We save everything and ...... it crashes with the following error:

```txt
Failed to compile.

Errors parsing template: Only void and foreign elements can be self closed "rect" ("  [ERROR ->]<rect
    width="300"
    height="100"
"): <your project dir>/src/app/line-plot/plot-area/plot-area.component.html@0:2
```

This error took me a while to figure out at the start, but it's fairly common when working with Dynamic SVGs in Angular. What is going on here? If we place the rect element as a child of an `svg` element it works fine, we just saw that. We broke it out to its own component and it doesn't work. This is because Angular does not see that this component will be used within the context of an `svg` element. Right now we could just drop this anywhere in our app and ask Angular to run it. It looked, and said:

> I don't know what a `<rect>` element is, and you can't self close it since I don't know what it is.

We can fix this very easily. SVG elements have a "Namespace" (Forgive me if that is not the right terminology). If we tell the template that we are using the SVG Namespace specifically, this will fix the error. Let's change the `plot-area.component.html` to the following:

**`plot-area.component.html`**

```html
<svg:rect
  width="300"
  height="100"
  style="fill: rgb(0, 0, 255); stroke-width: 3; stroke: rgb(0, 0, 0);"
/>
```

The prefixed `svg:` says:

> Look for this element with all the svg elements, not the HTML elements.

When we save, it compiles now.

## Adding Child to Parent

Normally, adding a child to a parent is really easy, just drop the child selector in the parent and away you go. Since we are working with SVGs this gets slightly more complicated. We are not working in the HTML context anymore and the SVG context can't add another element as easily as HTML can so we have to find a workaround. We can prove this by adding the `app-plot-area` selector to the `line-plot.component.html` like this:

**`line-plot.component.html`**

```html
<svg width="100%" height="100%" style="background-color: aqua;">
  <app-plot-area></app-plot-area>
</svg>
```

When we save it... _compiles?_ Yes, because from an HTML perspective, we didn't actually do anything wrong. We can add an `app-plot-area` selector into an `XML`-like document right there. If we look at the web page, you will not see the dark blue rectangle still. From an HTML perspective everything is hunky dory. The SVG element doesn't have any idea what to do with the `app-plot-area` element so it chooses not to render it. We still need this component to break up our parent component into manageable pieces, so how do we work around this? We need to use an element that SVG does understand: The `g` element. SVG Groups allow us to bring in another component. The final step is to tell the child component that it can attach to a different type of element than the `plot-area` one. We can do this by adding square braces around the selector, much like a directive.

**`plot-area.component.ts`**

```ts
import { Component, OnInit } from '@angular/core';

@Component({
  selector: '[app-plot-area]',
  templateUrl: './plot-area.component.html',
  styleUrls: ['./plot-area.component.scss']
})
export class PlotAreaComponent implements OnInit {
  constructor() {}

  ngOnInit(): void {}
}
```

If you have ts-lint running it will probably yell at you for doing this. Since we know we are not making a mistake, we can disable the component selector rule by adding:

```ts
// tslint:disable-next-line: component-selector
```

to the line above the the selector.

Let's modify the `line-plot.component.ts` to use this child component now:

**`line-plot.component.ts`**

```html
<svg width="100%" height="100%" style="background-color: aqua;">
  <g app-plot-area></g>
</svg>
```

Save all files and voila!! You have a parent child relationship using SVGs! Hope you enjoyed this article. Next article we will work on some data binding nuances with SVGs and Angular.

---
title: 'HTML For Humans - 4 - HTML Text Elements'
date: '2020-03-01T23:50:38.121Z'
template: 'post'
draft: false
slug: 'html-text-elements'
category: 'HTML For Humans'
tags:
  - 'HTML'
  - 'HTML For Humans'
  - 'Text'
description: 'We discuss the various HTML text tags and how to use them.'
socialImage: '/media/covers/html-for-humans/html-text-cover.jpg'
---

![First HTML Cover](/media/covers/html-for-humans/html-text-cover.jpg)

<center>Photo by Romain Vignes on Unsplash</center>

## Table of Contents

**[HTML Tags And Elements](#html-tags-and-elements)**

**[Starting Big - Headers](#starting-big---headers)**

**[Paragraph Tag](#paragraph-tag)**

**[Quotes](#quotes)**

**[Links - Anchor Tag](#links---anchor-tag)**

**[Conclusion](#conclusion)**

This is when things start to get fun! This article we'll talk about different text elements that can be used in HTML files. If you missed the link in the last post, the code to follow along with is located at [this GitHub page](https://github.com/hawkeye2013/HTML-For-Humans). You can find it in the `4 - HTML Text Elements` folder.

## HTML Tags And Elements

The last article we breezed over the whole concept of the HTML Tags and Elements. That is an important concept so we'll cover that now. Take a look at the following `<title>` tag. We talked about this tag in the last article but in case you missed it, the `<title>` tag displays the title of the site in the tab header.

```html
<title>Site Title</title>
```

**Elements** - HTML Tags are the building block of websites. The whole example above is an **HTML Element**. HTML elements are usually made up of an opening tag, content and a closing tag.

**Tag** - In the example, the `<title>` is the **opening tag** and the `</title>` is the **closing tag**.

## Starting Big - Headers

The first set of elements we'll talk about are the header elements. As you may imagine, these are the largest elements of the page. There are six levels of headers. From largest to smallest, these are `h1` - `h6`. Using the template we had from the last article, type the following between the `<body> </body>` tags.

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Document Name</title>
  </head>
  <body>
    <h1>This is a Heading 1</h1>
    <h2>This is a Heading 2</h2>
    <h3>This is a Heading 3</h3>
    <h4>This is a Heading 4</h4>
    <h5>This is a Heading 5</h5>
    <h6>This is a Heading 6</h6>
  </body>
</html>
```

Open the file in a browser and take a look at what they look like. You should have a similar output to below.

![Heading Output](/assets/html-text-elements/heading-output.png)

There should only be one `h1` element on the page at a time. Search engines look for the `h1` element when they are indexing the page. If you have more than one, the search engine will not know what to do!

All other headings should follow a hierarchical structure in order of importance. For instance, the `h2`s should be "more important" than the `h3`s. We will walk through some tutorials that make a little how these should be set up a little more clear.

## Paragraph Tag

Paragraph tags are all over in HTML. As you might guess, these hold the large groups of text. Here is what they look like:

```html
<p>This is a paragraph tag!</p>
```

When you type that in and refresh the page, you should some smaller text under the headings.

## Quotes

Quotes are shown using the `blockquote` tag. Go ahead and type out the following under the paragraph tag:

```html
<blockquote>
  Be yourself; everyone else is already taken. - Oscar Wilde
</blockquote>
```

For now, this doesn't look like much of a change other than a slight indent. In the next section where we talk about CSS and styling, we will take another look at the `blockquote` tag and format it to look more like a quote.

I want to mention a note about the whitespace in HTML. In programming, whitespace is considered all the spaces and newlines between tags and elements. In HTML, whitespace is only important in one case: The first space in between words. Take a look at the following examples.

```html
<blockquote>
  Be yourself; everyone else is already taken. - Oscar Wilde
</blockquote>
```

<!-- prettier-ignore -->
```html
<blockquote>Be yourself; everyone else is already taken. - Oscar Wilde</blockquote>
```

<!-- prettier-ignore -->
```html
<blockquote>Be yourself; everyone else is already taken.          - Oscar Wilde</blockquote>
```

If you type all three of these into the HTML file, they will render the same in the browser. This is because the first space between words is the only thing that is rendered, all other whitespace is ignored by the computer. There are some languages, such as Python, that will not run unless the files are formatted correctly. HTML is formatted to allow quick visualizations of the hierarchy and relationships of elements. We'll talk about that more later!

## Links - Anchor Tag

Anchor tags define links. Links introduce a new concept for us: **The HTML Attribute**. Take a look at the following anchor tag.

```html
<a href="https://google.com">Google</a>
```

This tag, unlike the last few, has something extra. The `<a>` and `</a>` work just like the paragraph tags above. Anything that is between those tags is rendered to the screen. The `href` portion of this tag is called an **attribute**. Attributes are not rendered to the page, but they provide additional information about the element. In this case, the information is where to go when it is clicked. We will see more attributes in the next article.

## Conclusion

We covered a lot in this article. We discussed the difference between HTML elements and tags, Headings, Paragraphs, quotes and links. Your code should look similar to below.

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Document Name</title>
  </head>
  <body>
    <!-- This is a comment: It is only a note for the developers and is ignored when running code -->

    <!-- Headings -->
    <h1>This is a Heading 1</h1>
    <h2>This is a Heading 2</h2>
    <h3>This is a Heading 3</h3>
    <h4>This is a Heading 4</h4>
    <h5>This is a Heading 5</h5>
    <h6>This is a Heading 6</h6>

    <!-- Paragraph Tags -->
    <p>This is a paragraph tag!</p>

    <!-- Blockquote -->
    <blockquote>
      Be yourself; everyone else is already taken. - Oscar Wilde
    </blockquote>

    <a href="https://google.com">Google</a>
  </body>
</html>
```

In the next article we will talk about putting images in our HTML pages!

[Previous Article](/posts/html-for-humans/our-first-html-file)

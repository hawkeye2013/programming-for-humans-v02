---
title: 'HTML For Humans - 3 - Our First HTML File'
date: '2020-03-01T23:50:37.121Z'
template: 'post'
draft: false
slug: 'our-first-html-file'
category: 'HTML For Humans'
tags:
  - 'HTML'
  - 'HTML For Humans'
description: 'We discuss the basic HTML template tags'
socialImage: '/media/covers/html-for-humans/first-html-cover.jpg'
---

![First HTML Cover](/media/covers/html-for-humans/first-html-cover.jpg)

<center>Photo by Florian Olivo on Unsplash</center>

## Table of Contents

**[Creating an HTML Document](#creating-an-html-document)**

**[Introducing The Standard Format](#introducing-the-standard-format)**

**[Conclusion](#conclusion)**

## Creating an HTML Document

We just got done talking about the difference between word processors and text editors. I am going to assume that you have downloaded a text editor and are up and running with it. If not, check out the [Previous Article](/posts/html-for-humans/working-with-text-editors).

With that out of the way, let's make our first HTML file! Your computer may not have a "New HTML" document button, so you may have to create an HTML file another way. These pictures are from a Windows computer, but a Mac has a similar process. This can also be done in the text editor, as we will do later, but it's important to know how to manipulate the operating system as well.

First, we will create a new text file by `Right Click -> New -> Text Document`.

![Create New File](/assets/new-file.png)

Next, while the rename is highlighted, we are going to delete everything **including** the `.txt` at the end. We will type `index.html` as the name. Commonly the home page of a website is named `index.html`, so we will follow convention here.

![Rename](/assets/rename.png)

If you hit enter too fast, just rename the file via `Right Click -> Rename` or hitting `F2` on the keyboard. Make sure you change the `.txt` to `.html`. Now you have an HTML file on your computer! Go ahead and open it up with your text editor of choice.

Before we go on, I want to point something out here. We not only changed the name of the file, but the file extension as well (`.txt` to `.html`). The file extension is the way that the operating system knows how to act when it opens up the file so this is an important step. If you do not do this, your browser will not understand that it is looking at something that can be shown as a web page.

We now have a blank page staring at us. We will edit within our text editor and test the code in the browser. The easiest way to open the file is `Right Click -> Open With` and choose your browser of choice. Chrome has, in my opinion, the best developer tools out there so I would recommend using that.

Now you should have a blank page on your text editor and a blank page open in your browser! Go ahead and type anything into the text editor and save the file. Refresh the page and poof! the text should show up in the browser!

### Introducing The Standard Format

Let's continue to create an HTML document. Although we are currently editing a file that has an HTML extension on it, every other HTML file out there will have a couple of extra things included, the standard format. Here is the template for it:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Document Name</title>
  </head>
  <body></body>
</html>
```

HTML has a standard way of writing files, the standard format. Let's break this down. The first tag, `<!DOCTYPE html>` is the document type. This tag is the first thing that should be in any HTML document. It defines what type of document it is for the browser.

The second tag is the `<html>` tag. This tag says that everything in between the opening tag `<html>` and the closing tag `</html>` should be treated as HTML.

The next tag is the `<head>` tag. This section is not rendered by the browser, so page content should not go into it. The head manages the metadata of the page. We will talk more about specific metadata later.

The next tag is the `<title>` tag. This tag defines the title of the website. The title is the text in the tab of the web browser. This might not seem like a big thing, but it's very important for search engines to index your page. This is part of the search engine optimization (SEO) algorithms. We will have an entire section on SEO optimization later. It is very important.

The final set of tags is are the `<body>` tags. The body holds all the content in the page. This is where 99% of the code you write will live.

From this point on we will use this standard format for all the files in the future, so it's good to know what each tag does!

## Github

Now that we have our first file with some code in it, I want to be able to have a comparison as you work through the content. I have created a [Github page for HTML For Humans](https://github.com/hawkeye2013/HTML-For-Humans). This is a public code repository where you can look at and download the code for your own use. There will be a `start` and `end` folder in each article so you can follow along with what I am doing. Enjoy!

## Conclusion

I wish there was a more exciting way to introduce the standard format but this is one of those foundational knowledge things that you just have to get through to get to the next step, kind of like Algebra II. I promise it will start to get more fun from here!

[Next Article](/posts/html-for-humans/html-text-elements)

[Previous Article](/posts/html-for-humans/working-with-text-editors)

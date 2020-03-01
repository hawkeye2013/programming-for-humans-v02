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
socialImage: '/assets/first-html-cover.jpg'
---

![First HTML Cover](/assets/first-html-cover.jpg)

<center>Photo by Florian Olivo on Unsplash</center>

## Creating an HTML Document

We just got done talking about the difference between word processors and text editors. I am going to assume that you have downloaded a text editor and are up and running with it.

With that out of the way, let's make our first HTML file! Your computer may not have a "New HTML" document button, so you may have to create an HTML file another way. These pictures are from a Windows computer, but a Mac has a similar process.

First, we will create a new text file.

![Create New File](/assets/new-file.png)

Next, while the rename is highlighted, we are going to delete everything including the `.txt` at the end. We will type `<yourFileName>.html` as the name substituting `<yourFileName>` with the file name of your choice. Commonly the home page is named `index.html`, so that is what I will name it here.

![Rename](/assets/rename.png)

If you hit enter too fast, just rename the file via `right click -> rename` or hitting `F2` on the keyboard. Now you have an HTML file on your computer! Go ahead and open it up with your text editor of choice.

We now have a blank page staring at us. We will edit within our text editor and test the code in the browser. The easiest way to open the file is `right click -> open with` and choose your browser of choice. Chrome has, in my opinion, the best developer tools out there so I would recommend using that.

Now you should have a blank page on your text editor, and a blank page open in your browser! Go ahead and type anything into the text editor and save the file. Refresh the page and poof! the text should show up in the browser!

### An HTML Document

Let's continue to create an HTML document. Although we are currently editing a file that has an HTML extension on it (the `.html` at the end of the file), every other HTML file out there will have a couple of extra things included, the standard format. Here is the template for it:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Document Name</title>
  </head>
  <body></body>
</html>
```

HTML has a standard way of writing files, the standard format. Let's break down what this means. The first tag is the doctype. This tag is the first thing that should be in any HTML document. It defines what type of document it is for the browser. The second tag is the `<html>` tag. This tag says that everything in between the opening tag `<html>` and the closing tag `</html>` is HTML. The next tag is the `<head>` tag. This section is not rendered by the browser, so content should not go into it. The head manages the metadata of the page. We will talk more about specific metadata later.

The next tag is the `<title>` tag. This tag defines the title of the website. The title is the text in the tab of the web browser. This might not seem like a big thing, but it's very important for search engines to index your page. This is part of the search engine optimization (SEO) algorithms.

The final set of tags is are the `<body>` tags. The body holds all the content in the page. This is where 99% of the code you write will live.

From this point on we will use this standard format for all the files in the future, so it's good to know what each tag does! They will make more sense as we make changes to them.

OK - Now we have the boring stuff out of the way, let's go make a real website!

[Previous Article](/posts/html-for-humans/working-with-text-editors)

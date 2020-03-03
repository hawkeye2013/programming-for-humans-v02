---
title: 'HTML For Humans - 2 - Working With Text Editors'
date: '2020-03-01T23:46:37.121Z'
template: 'post'
draft: false
slug: 'working-with-text-editors'
category: 'HTML For Humans'
tags:
  - 'HTML'
  - 'HTML For Humans'
  - 'Text Editors'
  - 'Word Processors'
description: 'We discuss the difference between a text editor and a word processor.'
socialImage: '/media/covers/html-for-humans/text-edit-cover.jpg'
---

![Text Edit Cover](/media/covers/html-for-humans/text-edit-cover.jpg)

<center>Photo by Sai Kiran Anagani on Unsplash</center>

## Table of Contents

**[Text Editors](#text-editors)**

**[Word Processors vs. Text Editors](#word-processor-vs-text-editor)**

**[Can I Use Notepad?](#can-i-use-notepad)**

**[Good Text Editors](#good-text-editors)**

**[Conclusion](#conclusion)**

## Text Editors

Let's discuss one of the primary tools of the web developer: The text editor.

Text editors are not something you would come across unless you are working with code. These are programs that edit just the content of the file without any shenanigans. Why would you need a special editor to write code? Code is just a bunch of files on your computer, so can't you just use any old editor? Wouldn't Microsoft Word work?

**NO**

Word will not work. Word is a word processor, not a text editor. Although they sound pretty close they are anything but.

## Word Processor vs. Text Editor

I have set up a little experiment here to prove the difference. I've opened a fresh Word document and typed a phrase in so it is not an empty document.

![Word](/assets/word.png)

I created another file with the same content. This file was created in Notepad.

![Notepad View](/assets/text-edit-words.png)

These two files were saved in the same folder. Take a look at the difference in sizes between the two documents.

![Files with both](/assets/folder.png)

The text document is weighing in at 28 bytes, pretty small. The Word document is 11.5 KB. A quick calculation says that the Word document is 410 times larger than the text document! But with the same content?

Let me explain.

Word documents just look like the text on a page. If you dig a little deeper, you can see they are split up into a ton of other files that define the data, the styles, the theme, etc... If you extract the Word document you can see this.

![extract dropdown](/assets/extract.png)

![extra folder.png](/assets/unzipped-word.png)

As you can see, when you extract the word document (as you would a zip file) it opens into a folder, this particular folder has 11 separate files in it. That is a ton of data for four words on a page. Word processors are used for manipulating text to publish. They handle styles, sizes, graphics, themes, etc. All that data would get in the way of what we need.

> Text.

> Pure. Beautiful. Sweet. Text.

## Can I use Notepad?

I mean, sure. If you want. I have seen notepad used before, but I absolutely would **not** recommend it. There are a bunch of awesome text editors out there with tons of tools to ensure that your code doesn't have simple errors in it. Notepad is not on that list.

## Good Text Editors

I have used all of these editors at one point or another and they all work well.

### [Brackets](http://brackets.io/)

Brackets is a pretty decent editor, made by adobe and released open-source. It works the way a text editor should. I do like the live preview feature, which launches a browser instance and reloads the page when you make a change. That feature was added to Visual Studio Code as an extension, so you don't get much more out of Brackets, but you should still try it and see if you like it.

### [Sublime Text](https://www.sublimetext.com/)

Sublime was the first text editor I used. It has some good features to it, but I don't think it's worth paying for it with the next two text editors on our list.

### [Atom](https://atom.io/)

Atom is one of my favorite editors. It's written by GitHub (We'll get to them soon). Its library of plugins makes it very easy to get syntax highlighting, language snippets, and many other things that make development easy.

### [Visual Studio Code](https://code.visualstudio.com/)

Visual Studio Code is by far my favorite text editor. It's authored by Microsoft and does just about everything right. The interface is intuitive and the minimalist design doesn't get in the way of programming. The thing that sets it apart is the integrated terminal. This makes life so much easier when working on large scale projects or more advanced frameworks and programs.

I would highly recommend that you download a couple, or all of these and try them out for yourself as you work through some of the projects on this site. Everyone is different and you may like an editor that I wasn't as big a fan of. Give it a go!

## Conclusion

In this article, we discussed using text editors to edit code. We also created a small example where we showed that a word document may say the same thing that a text file does, but there is much more going on with it. Check out the other articles below to continue learning about HTML.

[Next Article](/posts/html-for-humans/our-first-html-file)

[Previous Article](/posts/html-for-humans/intro-to-html)

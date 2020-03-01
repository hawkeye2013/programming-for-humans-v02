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
socialImage: '/assets/text-edit-cover.jpg'
---

![Text Edit Cover](/assets/text-edit-cover.jpg)

<center>Photo by Sai Kiran Anagani on Unsplash</center>

## Text Editors

Why would you need a special editor to write code? Code is just a bunch of files on your computer, so can't you just use any old editor? Wouldn't Microsoft Word work?

**NO**

Word will not work. Word is a word processor, not a text editor. Although they sound pretty close they are anything but.

### Word Processor vs. Text Editor

Ok, so I have set up a little experiment here. I've opened a fresh Word document and typed a phrase in so it is not an empty document.

![Word](/assets/word.png)

I created another file with the same content. This file was created in Notepad.

![Notepad View](/assets/text-edit-words.png)

These two files were saved in the same folder. Take a look at the difference in sizes between the two documents.

![Files with both](/assets/folder.png)

The text document is weighing in at 28 bytes, pretty small. The Word document is 11.5 KB. A quick calculation says that the Word document is 410 times larger than the text document! But with the same content?

Word documents just look like the text on a page. If you dig a little deeper, you can see they are split up into a ton of other files that define the data, the styles, the theme, etc... If you extract the Word document you can see this.

![extract dropdown](/assets/extract.png)

![extra folder.png](/assets/unzipped-word.png)

As you can see, when you extract the word document (as you would a zip file) it opens into a folder, this particular folder has 11 separate files in it. That is a ton of data for four words on a page.

Now let's circle back to word processors vs text editors. Word processors are used for manipulating text to publish. They handle styles, sizes, graphics, themes, etc. All that data would get in the way of what we need.

Text.

Pure. Beautiful. Sweet. Text.

### Can I use Notepad?

I mean, sure. If you want. I have seen notepad used before, but I absolutely would **not** recommend it. There are a bunch of awesome text editors out there with tons of tools to ensure that your code doesn't have simple errors in it.

### Good Text Editors

I have used all of these editors at one point or another and they all work well.

#### [Brackets](http://brackets.io/)

Brackets is a pretty decent editor, made by adobe and released open-source. It works the way a text editor should. I do like the live preview feature, which launches a browser instance and reloads the page when you make a change.

#### [Sublime Text](https://www.sublimetext.com/)

Sublime was the first text editor I used. It has some good features to it, but I don't think it's worth paying for it with the next two text editors on our list.

#### [Atom](https://atom.io/)

Atom is one of my favorite editors. It's written by GitHub (We'll get to them soon). Its library of plugins makes it very easy to get syntax highlighting, language snippets, and many other things that make development easy.

#### [Visual Studio Code](https://code.visualstudio.com/)

Visual Studio Code is by far my favorite text editor. It's authored by Microsoft and does just about everything right. The interface is intuitive and the minimalist design doesn't get in the way of programming. The thing that sets it apart is the integrated terminal. This makes life SO much easier when working on large scale projects or more advanced frameworks and programs.

I would highly recommend that you download a couple, or all of these and try them out for yourself as you work through some of the projects on this site. Everyone is different and you may like an editor that I wasn't as big a fan of. Give it a go!

[Previous Article](/posts/html-for-humans/intro-to-html)

[Next Article](/posts/html-for-humans/our-first-html-file)

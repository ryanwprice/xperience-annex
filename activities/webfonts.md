---
title: Web Fonts
category: three
description: >-
  Using your knowledge of type on the Web from last week, now we will expand on
  that knowledge with Web fonts.
graded: false
sidebar: This activity is to be completed individually.
published: true
---

This is your opportunity to apply special typefaces that are hosted by
Google's webfont service

## Exercise:

### 1. Style your doc

Using the index.html and style.css files in [webfonts.zip]({{ site.github.url }}/assets/webfonts.zip), add some CSS properties to improve the default typography. Consider size, spacing, colour, etc. and create a design that helps improve the communication of the document while looking good as well.

Before you get going, don't forget to setup the site and open the root folder in Brackets.

### 2. Add a webfont

Visit the [Google web fonts](http://www.google.com/webfonts) site and select one of the 818 (at the time of writing) fonts available. Click the "+" button (top right of the font). A black box entitled "Families Selected" will appear at the bottom of the screen.

![]({{ site.github.url }}/images/webfonts-step01.png)

### 3. Add the code

Follow the instructions under the "Embed" tab to add a stylesheet link to request the desired webfont. It should look similar to the one below

    <link rel="stylesheet" type="text/css" href="http://fonts.googleapis.com/css?family=Font+Name">

### 4. Style an Element

Whether you have selected the a headline or paragraph text, you need to apply the font to your CSS file. Take a look at the example below for help. The specific font name will be provided by Google.

    h1{ font-family: 'Google Webfont name', serif; }

### 5. One more thing!

Now that you've added a webfont, why not add some CSS3? Give the text-shadow property a whirl (as seen below):

![]({{ site.github.url }}/images/webfonts-step02.png)

## Submission:

Call Ryan over to show how awesome you are! You're done!

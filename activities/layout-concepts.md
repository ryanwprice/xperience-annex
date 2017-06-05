---
title: Layout Concepts
graded: n
---

There are all kinds of tools at our disposal to take our headings,
images, and text and fit them on the page, just the same way we can in
print layout programs like InDesign.

## To the left

To start, download the [layout-concepts.zip](/assets/layout-concepts.zip)
file and manage the site in Dreamweaver.

There are six mini activities to work through.

## 01 — Boxes

Width and Height can be applied to elements as px or percentages. We can
style the .box div with a pixel-width and height, and we can use
percentages for the paragraphs.

    .box{
      height:300px;
      width: 300px;
      background-color:red;
    }

    p.one, .two{
      height: 75%;
      width: 75%;
      background-color: yellow;
      margin:0; 
    }

![](/images/concepts-box01.jpg)

Notice how the text in the second paragraph takes up more space then the
size of the box we created?

With a little bit of CSS, we can fix that.

    .two{
      overflow:hidden;
    }

    .two{
      overflow:scroll;
    }

[![](/images/concepts-box02.jpg)](images/concepts-box02.jpg)

Left: `overflow:hidden`, Right: `overflow:scroll`

## 02 — Borders

We've looked at borders before, so we won't get caught up here. Here's
some code:

    p{
      padding:10px;
      border: 2px solid red;
      border: 2px dashed green;
      border-left: 4px dotted blue;
      border-bottom:10px solid black;
    }

And here is the output in the browser.

[![](/images/concepts-borders.jpg)](images/concepts-borders.jpg)

We can change the style of the border (dotted, dashed, etc.), the
colour, and we can even target just one side at a time if we wanna get
real fancy!

### 03 — Inline vs Block

Some elements will always appear to continue on the same line as their
neighbouring elements. These are inline.

Typically, inline elements sit inside a block element (ex: `<strong>`,
`<em>`, `<a>`, etc. are part of a `<p>`

### HTML

    <a href="#">link one</a>
    <a href="#">link two</a>
    <a href="#">link three</a>

### Browser

![](/images/concepts-inline.jpg)

The code above displays like this in the browser.

Some elements will always appear to start on a new line in the browser.
These are block elements. ex: `<p> <h1> <ul> <li>` etc.

### HTML

    <p>One</p>
    <p>Two</p>
    <p>Three</p>

### Browser

![](/images/concepts-block.jpg)

The code above displays like this in the browser.

With the Box Model, we can add a border, padding, margins, even width
and height to an element. As we add these elements, the actual size of
the element grows in the browser. The element is the sum of all of it's
parts

### HTML

    <p class="box">One</p>
    <p class="box">Two</p>
    <p class="box">Three</p>

#### CSS

    .box{
      border:1px solid red;
      width:100px;
      padding:10px;
      margin:20px;
      background-color: #ccc;
      float: left;
    }

### Browser

![](/images/concepts-boxmodel.jpg)

Each paragraph occupies 166px of width (margin left & right, padding
left & right, border left & right, and width).

Need a little more info on the Box Model? Try the [Box
Model](boxmodel.html) activity from week four.

### 04 — Floats

Floats let us do just as the suggest, float items left and right.

    p{
      width:180px;
      float: left;
      margin:10px;
      background-color: yellow;
    }

[![](/images/concepts-floats.jpg)](/images/concepts-floats.jpg)

The `float` property allows our 180-pixel-wide paragraphs to float to
the left of the one before. Try resizing the browser; as it gets
smaller, the paragraphs will fall under each other when there is no
space for them to float left.

The `margin` puts space between each paragraph/column. Try taking it out
and see what happens when you refresh.

A `background-color` has been added to make things easier to see.

## 05 — Image floats

Start by inserting an image inside the start of the first paragraph.
Images are inline elements, so they fit nicely in paragraphs, which are
block elements.

    <p><img src="images/starfish.jpg"/>Lorem ipsum dolor...

If we add in some CSS, we can see how the image floats within the text.

    img{
      float: left;
      padding: 4px;
      border: 1px solid red;
      margin:0 10px 10px 0;
    }

Try resizing the browser and see how the text wraps around the image,
just like a text wrap in InDesign.

[![](/images/concepts-images01.jpg)](/images/concepts-images01.jpg)

Now try changing the `float` from left to right.

[![](/images/concepts-images02.jpg)](/images/concepts-images02.jpg)

Now let's take out that img tag and move it into a `figure`.

    <figure>
      <img src="images/starfish.jpg"/>
      <figcaption>This is a red starfish</figcaption>
    </figure>
    <p><img src="images/starfish.jpg"/>Lorem ipsum dolor...

Now, if we add a bit of CSS we can create an image sidebar. The `figure`
tag acts like a group container for the `img` and `figcaption`

    figure{
      float: right;
      width:400px;
    }

[![](/images/concepts-images03.jpg)](/images/concepts-images03.jpg)

Now, let's remove the figure all together—but with CSS!

    figure{
        display:none;
    }

This little trick is very powerful. Anything that you remove this way
becomes invisible to screen readers and search engines, but someone can
still find it in the source code if they go looking. Use sparingly!

Let's throw three thumbnails in at top of the `body`, just above our
figure.

    <img src="images/thumb01.jpg" />
    <img src="images/thumb02.jpg" />
    <img src="images/thumb03.jpg" />

[![](/images/concepts-images04.jpg)](/images/concepts-images04.jpg)

Nothin' fancy, so let's keep going!

With a bit of CSS code we can create a stack of images.

    img{
      float: right;
      margin:0 0 10px 10px;
      clear: right;
    }

We floated all images to the right, and then forced each image to clear
any element floated to the right. To finish it off, we put 10px of
margin on the bottom and right of each image to add a bit of breathing
room.

[![](/images/concepts-images05.jpg)](/images/concepts-images05.jpg)

Just a tiny bit of code can go a long way!

## 06 — Positioning

Our HTML file already has some CSS in it to create four boxes, each
100px square.

[![](/images/concepts-positioning01.jpg)](/images/concepts-positioning01.jpg)

Little boxes made of ticky-tacky.

Up until now, everything we've looked at has been Relative to the item
before and after it. Now we can position items absolutely so they sit
exactly where we want them.

To do that, we need to do two things: declare the items to be absolute
and give them coordinates.

    .red, .green, .blue, .black{
      position:absolute;
    }

    .red{
      top: 10px;
      left: 10px;
    }

    .green{
      top:10px;
      right:10px;
    }

    .blue{
      bottom: 10px;
      left:10px;
    }

    .black{
      top: 55px;
      left: 55px;
    }

[![](/images/concepts-positioning02.jpg)](/images/concepts-positioning02.jpg)

Try resizing the browser. No matter what size the window is, the boxes
sit exactly where we told them to.

Using absolute positioning is *very powerful* and should be used
sparingly. It can often times lead to more headaches than it's worth!

Our black square overlaps the red square, and so it should because it
was the last thing in our HTML code to be rendered. We can fix that with
CSS.

    .red{
      top: 10px;
      left: 10px;
      z-index: 1;
    }

[![](/images/concepts-positioning03.jpg)](/images/concepts-positioning03.jpg)

Just like layers in Photoshop, we can move items up and down and control
overlap.

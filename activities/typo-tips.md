---
title: Erik Spiekermann’s Typo Tips
graded: n
---

Erik Spiekermann is considered a type legend. He is the author of _Stop Stealing Sheep_, a quintessential textbook on typography, founder of the _FontShop_ type foundry, and a type designer of several famous typefaces, to boot. Given Spiekermann’s type successes, it might be worth taking note of what he has to say. For this exercise we will be applying CSS code to make his _Typo Tips_ more aesthetically pleasing.

To start this activity, you will need the [typo-tips.zip]({{ site.github.url }}/assets/typo-tips.zip) file. Download it, unzip it, and then Manage the Site in your code editor (Atom, Dreamweaver, etc.).

Before we start coding, you might notice that the root folder has an images and styles folder inside it, as well as an `index.html` file. This is the standard folder & file structure for a small Web site. 

The `index.html` file is the “home page” and is where the actual text resides. Load that up in the browser (double-click it). 

The _images_ folder would hold any images we might use for the site. The _styles_ folder holds our CSS. If you look inside that folder, you will will see a `style.css` file. This is the file we will add all of our code to for this exercise.

## A little goes a long way

The HTML file already has a div with the id of `#wrapper` in place. Let's start by setting a width and making the line-length (AKA the measure) of our text more readable by adding the following code to our CSS file.

    #wrapper{
      width:600px;
      margin: 0 auto;
    }

Next we want to select a typeface by adding a font-family to our code. We could apply the same font stack to each element on the page (`h1`, `h2`, `p`, etc.) or we could use the power of the *Cascading* Style Sheet and apply our fonts to the body and have everything nested within the body inherit those fonts.

    body{
        font-family: Georgia, Times, "Times New Roman", serif;
    }

Remember to put the quotes around any fonts that are more than one word; I'm lookin' at you, Times New Roman!

Next, we will create some contrast between our paragraphs and headings, to help improve the hierarchy with visual cues.

    h1, h2, h3{
      font-family: Helvetica, Arial, sans-serif;
    }

Make sure you always finish a font stack with a generic font type like `sans-serif`, `serif`, `script`, etc.

To save time and space, we can apply the font-family to the `h1`, `h2`, and `h3`, simply by putting commas between them.

Next, we will add some size/scale to our headings to refine our hierarchy a little further. We'll also apply some margins (invisible gutters) around our text.

    h1{
      font-size: 36px;
      margin-bottom: 12px;
    }

    h2{
      font-size:28px;
    }

    h3{
      font-size:24px;
      margin:36px 0 0 0;
    }

Margins work just like a clock — our margins starts at 12 o'clock and move clockwise — Top, Right, Bottom, Left.

Now let's tweak the paragraphs.

    p{
      font-size: 16px;
      margin:18px 0;
      line-height: 22px;
    }

Line-height is like the baseline in InDesign, but instead of sitting at the bottom (or the baseline) of the text, it calculates the distance between lines of text from their centres.

## Fine-tuning the fonts

A few more lines of CSS to fine-tune our type (and give us the chance to try out a whack of other css properties).

    h1{
      text-align: center;
      text-transform: capitalize;
    }

    h2{
      text-align: center;
      font-style: italic;
      font-weight: normal;
    }

    h3{
      text-transform: capitalize;
    }

    p{
      text-indent: 15px;
    }

Now we'll add some colour to the text. Make sure you apply this code inside your existing elements, rather than simply cutting and pasting from below.

### It's all in the details

All of the colours are hexidecimal representations of Crayola colours. Check out the linked site, if you'd like to check out the [Crayola colour codes](http://www.colourlovers.com/web/blog/2008/04/22/all-120-crayon-names-color-codes-and-fun-facts).

    h1{
      color: #FF496C;
    }

    h2{
      color: #EF98AA;
    }

    h3{
      color: #FC2847;
    }
    
If the colours aren’t working for you, go back to your CSS code and make sure you used the correct spelling: “color” not “colo**u**r”.

Finally, let's add some minor details to really perfect our design.

    .no-indent{
      text-indent: 0;
    }

    a{
      color: #EE204D;
      text-decoration: none;
    }
    
The above code took the underline off of our links, added small-caps to any tag with the class of `.credits`, and removed indentation from any tag with a class of `.no-indent`

There’s one final step, and it is the most important: Save your work!
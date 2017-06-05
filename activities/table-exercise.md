---
title: Tables Exercise
graded: n
---

Before we start, we need to setup a new site. Download the
[generic-site-template.zip]({{ site.github.url }}/assets/generic-site-template.zip) for all
the necessary files & folders.

Let's start by building a simple table with 3 bands and 3 albums.

The table will have three rows, known as `<tr>`s, and each row will have
2 columns, known as `<td>`s

    <table>
        <tr>
            <td>Nirvana</td>
            <td>In Utero</td>
        </tr>
        <tr>
            <td>Adele</td>
            <td>21</td>
        </tr>
        <tr>
            <td>Pink Floyd</td>
            <td>The Wall</td>
        </tr>
    </table>

## Let's complicate matters

Now that we have a simple table, we can add a header to our table to
give our columns titles.

We will simply add another table row with 2 `<th>`s instead of `<td>`s

    <table>
        <tr>
            <th>Band</th>
            <th>Album</th>
        </tr>
        <tr>
            <td>Nirvana</td>
            <td>In Utero</td>
        </tr>
        <tr>
            <td>Adele</td>
            <td>21</td>
        </tr>
        <tr>
            <td>Pink Floyd</td>
            <td>The Wall</td>
        </tr>
    </table>

## Just a little more markup

Our code works, but we still need to add our sections to divide the head
and the body. We need to nest our header and body in `<thead>` and
`<tbody>`, respectively.

    <table>
        <thead>
            <tr>
                <th>Band</th>
                <th>Album</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Nirvana</td>
                <td>In Utero</td>
            </tr>
            <tr>
                <td>Adele</td>
                <td>21</td>
            </tr>
            <tr>
                <td>Pink Floyd</td>
                <td>The Wall</td>
            </tr>
        </tbody>
    </table>

## Just for kicks!

Now that our table has content, titles for the columns, we can go and
add a footer. The `tfoot` will just have some extra info about our
musical choices, so it can occupy both columns by using a `colspan`.

    <table>
        <thead>
            <tr>
                <th>Band</th>
                <th>Album</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Nirvana</td>
                <td>In Utero</td>
            </tr>
            <tr>
                <td>Adele</td>
                <td>21</td>
            </tr>
            <tr>
                <td>Pink Floyd</td>
                <td>The Wall</td>
            </tr>
        </tbody>
        <tfoot>
            <tr>
                <td colspan=2>Albums selected at random</td>
            </tr>
        </tfoot>
    </table>

## Style it up!

We have a table, albeit an ugly one. We can add some style to our css
file.

    table{
        border-collapse: collapse;
        font-family: Helvetica, Arial, sans-serif;
    }

    td, th{
        border: 1px solid black;
        padding: 4px;
    }   

Try the CSS without the `border-collapse` and see how you get odd little
margins between each cell.

Now let's style the header...

    th{
        background-color: #333;
        color: white;
        font-weight:bold;
        text-align: left;
    }

The header, by default is centred, so we need to align it left.

Now we can set the size of our table

    table{
        border-collapse: collapse;
        font-family: Helvetica, Arial, sans-serif;
        width: 400px;
    }

    td, th{
        border: 1px solid black;
        padding: 4px;
        width: 50%;
        height: 60px;
        vertical-align: center;
    }

By default, most browsers set the vertical alignment to center, but we
want to ensure the design looks right.

Last, but not least, we can throw some style at our footer.

    tfoot{
        text-align: center;
        font-style: italic;
        color: #666;
    }

## Extra! Extra!

If our list was longer, we might decide to add alternating stripes to
our rows to make the list easier to read. We could apply a class to
every odd row with a name like "odd". Our code would look something like
this:

    <table>
        <thead>
            <tr>
                <th>Band</th>
                <th>Album</th>
            </tr>
        </thead>
        <tbody>
            <tr class="odd">
                <td>Nirvana</td>
                <td>In Utero</td>
            </tr>
            <tr>
                <td>Adele</td>
                <td>21</td>
            </tr>
            <tr class="odd">
                <td>Pink Floyd</td>
                <td>The Wall</td>
            </tr>
        </tbody>
        <tfoot>
            <tr>
                <td colspan=2>Albums selected at random</td>
            </tr>
        </tfoot>
    </table>

Remember, we can use a class as many times as we like.

Now we can create some CSS for it.

    .odd{
        background-color:#DDD;
    }

These alternating bars of colour are often referred to as “zebra
stripes”
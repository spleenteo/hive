Hive
====

What the Hive is this!?
-----------------------
We are in the "responsive" Era! So many devices that we cannot design for specific sizes or smartphone/tablets models.
Bees are able to build a hive as a pattern based either on their number and on the stage they are going to do it.
A grid layout should be almost the same: help us to adapt content to the viewport the website is shown on.
So I wrote some media queries to break-up the layout on four different sizes: smartphone portrait, landscape, tablets portrait, desktop and cinema display. All these breaks can be easly changed on the SCSS file.

So, Hive is a CSS grid system originaly inspired by the more famous [960grid](http://960.gs/).
The naming of wrappers and grids has been changed to use the metaphor of hives and cells.
Using just one markup you can have a responsive (mobile-ready) fluid layout (with a preferred % width).
This system is written in SCSS but the repo includes a ready to use CSS file.

Features
--------

* SCSS grid system
* no gutter between columns
* Responsive ready for mobile / tablets / desktop / cinema display design
* variable fluid template structure (you can changed it on the fly)
* 12 or 16 columns layout
* easy to change the breakup media queries

Installation
------------

Hive is written in SCSS, so you need a [Sass](http://sass-lang.com/) interpreter to export the final CSS file.
In any case you can use the CSS file, but you'll lose the possibility to change the parameters to get a variable width on a fluid template.
I use the [Haml](http://haml-lang.com/) ruby gem as a Sass interpreter. This is the command

    $ sass -C -t compact --watch [the/scss/main/directory/path]:[your/website/css/directory]

Classes
-------

If you are a 960grid user you'll know the two main classes .container_* and .grid_*
In Hive there is the same basic concept with different names:

* .hive_12 and .hive_16 for containers
* .cell_[from 1 to 12/16] for grids

Example
-------

    <body>
        <div class="hive_12">
            <hgroup>
                <div class="cell_6">
                    <h1>
                        text on the left
                    </h1>
                </div>
                <div class="cell_6">
                    <h2 class="cell_6">
                        text on the right side
                    </h2>
                </div>
            </hgroup>
            <div class="cell_12">
                <article>
                    wide content
                </article>
            </div>
        </div>
    </body>

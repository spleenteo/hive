# Hive

## What the Hive is this!?

Just another grid system to build responsive layout.
The naming of wrappers and grids has been changed to use the metaphor of hives and cells.
Bees are able to build a hive as a pattern based either on their number and on the stage they are going to do it.
Using just one markup you can have a responsive (mobile-ready) fluid layout (with a preferred % width).
This system is written in SCSS but the repo includes a ready to use CSS file.

## The new release

The first version of hive was base on 12 or 16 columns as it was inspired by 960grid. You could choose your width, in percentage or fixed pixel than build your layout thinking in 12 or 16. So, to make a column the half of the hive, a .cell_6 was supposed to be used.

Now everything is changed! We want to be responsive, we don't know the px width of the breaks. So we could think in percentage. Thats why now hive is basically 100% width and can be splitted in 10 columns 10% each. There a few additional sizes, like 25% 33% 66% 75% that make we able to build 3 and 4 columns layouts.
Cells can be nested and nested again. Every time the cell_50 will be the 50% of it's container.

## Features

* SCSS/SASS grid system
* no gutter between columns
* Responsive ready for mobile / tablets / desktop / cinema display design
* variable fluid template structure (you can changed it on the fly)
* 12 or 16 columns layout
* easy to change the breakup media queries

# How to use it

Hive is written in SCSS, so you need a [Sass](http://sass-lang.com/) interpreter to export the final CSS file.

Warning!!!
since hive use variables to define some @media queries, you must use at least this version of sass gem to modify and compile hive

 Sass 3.2.0.alpha.244

In any case you can use the CSS file, but you'll lose the possibility to change the parameters to get a variable width on a fluid template.
I use the [Haml](http://haml-lang.com/) ruby gem as a Sass interpreter. This is the command

  $ sass -C -t compact --watch [the/scss/main/directory/path]:[your/website/css/directory]

## Classes

* .hive for containers
* .cell_[from 1 to 10/100] for columns


Example
-------

    <body>
        <div class="hive">
            <hgroup>
                <div class="cell_50">
                    <h1>
                        text on the left
                    </h1>
                </div>
                <div class="cell_50">
                    <h2>
                        text on the right side
                    </h2>
                </div>
            </hgroup>
            <div class="cell_100">
                <article>
                    wide content
                </article>
            </div>
            <div class="cell_33">
                one third box
            </div>
            <div class="cell_33">
                one third box
            </div>
            <div class="cell_33">
                one third box
            </div>
        </div>
    </body>

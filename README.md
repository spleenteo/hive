# Hive

## What the Hive is this!?

Just another grid system to build responsive layout! Yes, another one! :)

The grids has been changed to use the metaphor of Hives and cells.
Bees are able to build a Hive as a pattern based either on their number and on the stage they are going to do it.
Using just one markup you can have a responsive (mobile-ready) fluid layout (with a preferred % width). If you don't want to be responsive you can cong Hive to be fixed.

This library is written in SCSS but the repo includes a ready to use CSS file.

## The new release 2.0

The first version of Hive was based on 12 or 16 columns as it was inspired by 960grid. You could choose your width, in percentage or fixed pixel than build your layout thinking in 12 or 16. So, to make a column the half of the Hive, a .cell_6 was supposed to be used.

Now everything is changed! We want to be responsive so we could think in percentage instead of columns or portion (like .one_half classes I saw around).
Thats why now Hive is basically 100% width and can be splitted in 10 columns 10% each. There are few additional sizes, like 25% 33% 66% 75% that make us able to build 3 and 4 columns layouts.
Cells can be nested and nested again. A cell_50 will be the 50% of it's container.

## Features

* SCSS grid system
* no gutter between columns
* Responsive ready for mobile / tablets / desktop / cinema display design
* variable fluid/fixed template structure (you can changed it on the fly)
* easy to change the breakup media queries
* Classes available to drw box at the same height

# How to use it

Hive is written in SCSS, so you need a [Sass](http://sass-lang.com/) interpreter to export the final CSS file.

Since Hive use variables to define some @media queries, you must use at least this version of sass gem to modify and compile Hive

 Sass 3.2.0.alpha.244

In any case you can use the CSS file, but you'll be not able to change the parameters to get a fixed or fluid template, media breake etc.

I use the [Haml](http://haml-lang.com/) ruby gem as a Sass interpreter. This is the bash command to use it

  $ sass -C -t compact --watch [the/scss/main/directory/path]:[your/website/css/directory]

## Classes

* .Hive for containers
* .cell_[from 10 to 100] for columns (steps by 10)
* box_[from 1 to 8] - the number is the unit of height. by default 1 unit is 150px, 2 units is 305px (unit * 2 + 5px margin) and so on.

## Warning!!!

* _cell_ and _box_ are just containers. Don't use additional classes or styles that could change their size like paddings, margins etc.
* always use a section or a div as first element insie a _cell_ or _box_ - give it a classname and style it from there.


###Example
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

## What about Sass?

I do prefer scss to sass. @makwvoid did convert in sass the first release of this library, hope he'll do it again! :)



Hive
====

What the Hive is this!?
-----------------------

A CSS grid system inspired by the more famous [960grid](http://960.gs/).
The naming of wrappers and grids has been changed to use the metaphor of hives and cells.
Using just one markup you can have a responsive (mobile-ready) fixed (with a preferred width in px) or fluid (with a preferred % width).
This system is written in SCSS but the repo includes a ready to use CSS file.

Features
--------

* SCSS grid system
* Flexible gutter between columns
* Responsive ready for mobile design
* Fixed or fluid template structure (you can changed it on the fly)

Installation
------------

Hive is written in SCSS, so you need a [Sass](http://sass-lang.com/) interpreter to export the final CSS file.
In any case you can use the CSS file, but you'll lose the possibility to change the parameters to get a fixed or fluid template.
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
     <hgroup class=".hive_12">
      <h1 class=".cell_6">
       text on the left
      </h1>
      <h2 class=".cell_6">
       text on the right side
      </h3>
     </hgroup>
    </body>

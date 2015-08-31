.. include:: <s5defs.txt>

=====================
 rst2odp Slide Shows
=====================

:Author: Matt Harrison
:Date:   2008-12-17

Intro to rst and the odp converter

.. class:: handout

  Everything that is in this block will only be in the notes.
  You can put these on each slide.

Simple Slides
-------------

Here's how to make easy slideshows in rst.  Here's a list:

* Part
* of
* a
* list

Image
-----

.. image:: img/test.png


--------

.. class:: center huge

A slide with centered, huge text and no title

Source code
-----------

.. code-block:: python

  def foo(bar, baz):
    fizzle(bar, baz)


More Source code
----------------

.. class:: small

    .. code-block:: c

        int
        main(void) {
            printf("Hello, world\n");
            return 0;
        }

Can specify font size
---------------------

.. class:: font-size:100pt

  Large text

Grids
-----


.. grid:: 2,3x1

  Put text in a second cell of 3 columns and 1 row

.. grid:: 4,1x4

  Text along bottow cell of 4 rows

Incremental Text
----------------

Due to "feature" in ODT spec, it only works (by clicks) on a paragraph or outline level.

.. class:: incremental

  * foo
  * bar
  * baz

Text styling
------------

:tiny:`Some tiny text` (can also do ``small``, ``big``, or ``huge``)

Some *strong text* and **emphasized text**

:orange:`s5defs.txt Colors are also supported`

.. slide-layout:: 2column

Multiple Columns
----------------

This text goes in the first column.

.. column:: 2

This text goes in the second column.

.. column:: 3

This text goes in the third column.

.. slide-layout:: 1column

Master Pages
-------------

Open(Libre)Office have the notion of Master Pages. If you have a template that has multiple master pages (click on Format -> Slide Design to see the templates. At the bottom is the name). To use a different template for a slide insert::

  .. slide-design:: template-name

*before* a title.

Creating slides
---------------

* install ``rst2odp``
* plain : ``rst2odp slides.rst output.odp``
* template : ``rst2odp slides.rst --template-file template/darkGradient.otp output.odp``
* fonts : ``rst2odp --font="Droid Sans" --mono-font="Droid Sana Mono" slides.rst output.odp``
* code highlighting style : ``rst2odp --pygments-style=bw slides.rst output.odp``

Thanks
------

Send feedback/suggestions my way

matthewharrison@gmail.com

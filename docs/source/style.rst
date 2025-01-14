:orphan:

This page shows style conventions used in these docs.  It will be
built with other pages and you can view it (at
docs/build/html/style.html). Unfortunately, because it's intentionally
not included in the published docs, it generates the annoying warning
"WARNING: document isn't included in any toctree".


Headings
!!!!!!!!

ReST heading levels are determined by the character used beneath text.
Within a file, each new character creates a new heading level.

This documentation uses the characters ``!``, ``@``, ``#``, and ``$``.
That is, the first four shifted digit characters across a US keyboard.

For example::

  A Heading
  !!!!!!!!!

  The first subheading
  @@@@@@@@@@@@@@@@@@@@

  The first subsubeheading
  ########################

  The second subheading
  @@@@@@@@@@@@@@@@@@@@@

  Another Heading
  !!!!!!!!!!!!!!!


To aid comprehension, the Text Styles section source looks like this::

    .. _text-styles-target:
    
    Text Styles
    !!!!!!!!!!!


.. _text-styles-target:

Text Styles
!!!!!!!!!!!

A cheat sheet for making references, links, and literals in sphinx.

* For external links, use ``target_``.

  * See ``epilog.rst`` for pre-defined links.
  * e.g, todo

* *Within* VA documentation, use ``.. _refname:`` to create link
  target, and use ``:ref:`refname``` to reference it.

  * Create explicit link targets for all headings.
  * Do not rely on the implicit targets created by sphinx because
    changing the heading will break the link.
  * e.g., ``:ref:`text-styles-target``` renders as
    :ref:`text-styles-target` and uses the heading text as
    the link name.
  * e.g., todo
  * Use class names verbatim when making link targets (e.g., todo).

* Use \* for attributes.

  * ``*attribute*`` renders as *attribute*.
  * e.g., todo

* Use double backticks for literals.

  * ````literal```` renders as ``literal``
  * e.g., todo


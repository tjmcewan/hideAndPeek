hideAndPeek
===========

Really small & simple jQuery plugin to truncate long text, but show it on mouse hover.

## Usage

Pick up the elements that might have long content and call `hideAndPeek()` on them:

    $("td").hideAndPeek();

Either put it at the bottom of the page, or wrap it in a function passed to jQuery (which will execute it when `document.ready` fires)

    jQuery(function() {
      $("td").hideAndPeek();
    });

## Configuration

To specify a non-default content length limit or 'more content' indicator, call it like so:

      $("td").hideAndPeek({ length: 10, indicator: "»" });

The defaults are: `{ length: 12, indicator: "…" }`.  **NB:** That's an actual ellipsis, so make sure your page is UTF-8 (or override it with three dots).

## Caveats

- It uses dumb truncation that doesn't respect word boundaries.
- It rewrites the element's contents instead of displaying an overlay, so the element's size may change on hover.

## Why [another][1] [jQuery][2] [truncating][3] [plugin][4]?

A friend asked for a simple favour with simple requirements.  The others are mostly too big, and none of them support showing the original content on mouse hover.

[1]: http://dotdotdot.frebsite.nl/
[2]: http://micjamking.github.io/succinct/
[3]: http://badonkatrunc.com/
[4]: https://github.com/tbasse/jquery-truncate

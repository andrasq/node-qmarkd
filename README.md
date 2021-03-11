qmarkdn
=======

Quick little cli tool to format markup kind of like markdown, visually like github, but with some
small differences.  It's a little abridged and a little warped compared to markdown.

This started out as two-hour hack to apply some simple formatting my document; since then
it's been minor bugfixes; oh, and tables support.

This is a work in progress.  It has rough edges, but is usable.  It's compatible enough
with github markdown to render a reasonably close likeness of most README files.

The syntax currently is slightly different from github, but it works the way I like it.  It
also has some extensions brought over from another tool of mine.  This is a work in progress
and may change as I add/alter features or change my mind.


    $ qmarkdn README.md > out.html


Installing
----------

To install via npm

    npm install -g qmarkdn

To install and use from the command line, copy the file `bin/qmarkdn` from the repo
into a directory on your `$PATH`, and make the file executable.

    #!/bin/sh
    url=https://raw.githubusercontent.com/andrasq/node-qmarkdn/master/bin/qmarkdn
    curl -s curl $url > qmarkdn
    chmod +x qmarkdn
    sudo mv qmarkdn /usr/local/bin/


Features
--------

- bold `* *`, Italics `_ _`, typewriter `` ``
- `# .. #####` h1-h5 headers
- code blocks
- bullet lists, numbered lists
- obfuscated email links
- url links
- `.I, .B` etc nroff-style markup
- `||` `|` limited tables support (no escaping)


Differences
-----------

- item lists are flat, do not nest
- `* *` is bold, not Italic


Changelog
---------

- 0.2.2 - try to add anchors to the section headings, better invalid option wording, `-fa` option
- 0.2.1 - fix program `--version`
- 0.2.0 - handle embedded []() images and urls, stop auto-expanding urls and email addresses
- 0.1.3 - `--version` switch
- 0.1.2 - support blank lines in code blocks


Todo
----

- add support for `>` quoted text


Related Work
------------

- marked
- markdown

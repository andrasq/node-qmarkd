qmarkdn
=======

Quick little hack to format markup kind of like markdown, rather like github, but with some
small differences.  It's a little abridged and a little warped compared to markdown.

**WORK IN PROGRESS**

The syntax currently is slightly different from github, but it works the way I like it.  It
also has some extensions brought over from another tool of mine.  This is a work in progress
and may change as I add/alter features or change my mind.


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

- bold `* *`, Italics `_ _`, teletype `` ``
- `h1 .. h5` headers
- code blocks
- bullet lists, numbered lists
- obfuscated email links
- url links
- `.I, .B` etc nroff-style markup


Differences
-----------

- item lists are flat, do not nest
- `* *` is bold, not Italic


Related Work
------------

- marked
- markdown

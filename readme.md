# smudge and clean

## the basic idea

git provides filters which you can access via
your `attributes` and `config` files.

This project sets up simple smudge and clean
filters to demonstrate how they work.

## context

More info here:

http://git-scm.com/book/ch7-2.html

## how it works

Filters are arbitrary Unix software. They must
conform to the standard interface for all Unix
software: take input via `stdin`, exit with a 0
for success or any number up to 255 for failure,
etc. The filters in this project are bash scripts,
but you could easily substitute a Node.js "binary"
prepared in the `npm` way, or a Ruby "binary"
prepared in the `gem` way.

The `clean` and `smudge` filters in this directory
run simple one-line Ruby scripts to convert tabs
into spaces when you check a file out, and convert
spaces into tabs when you commit a file.

The files `git.config.sample` and
`git.attributes.sample` demo what your `config`
and `attributes` files should look like in
order to make this work. Those files live at
either `.git/info/attributes` (project-local)
or `.gitattributes` (global), for `attributes`,
and either `.git/config` (project-local) or
`.gitconfig` (global), for `config`.


# smudge and clean

git provides filters which you can access via
`.git/info/attributes` (project-local) or
`.gitattributes` (global) and `.git/config`
(project-local) or `.gitconfig` (global). This
project sets up simple smudge and clean filters to
demonstrate how they work.

Filters are arbitrary Unix software. They must
conform to the standard interface for all Unix
software: take input via `stdin`, exit with a 0
for success or any number up to 255 for failure,
etc. The filters in this project are bash scripts,
but you could easily substitute a Node.js "binary"
prepared in the `npm` way, or a Ruby "binary"
prepared in the `gem` way.

The files `git.config.sample` and
`git.attributes.sample` hopefully serve an obvious
purpose.


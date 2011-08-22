# Bundler Path Helpers

These functions will automatically add and remove bundled gems and binaries
to your `$GEM_PATH` and `$PATH` respectively. They are run every time you change
directories.

## Conventions

* Your bundled gems must be stored in `vendor/bundle`
* You use `zsh`
* Your have a properly configured `$fpath`

## Installation

Clone the respository somewhere.

    $ cd ~/.zsh/plugins; git clone git://github.com/lordzork/zsh-bundler-path-helpers.git

Link it into your `$fpath`.

    $ ln -s plugins/zsh-bundler-path-helpers/functions functions/bundler-path-helpers

You should have `zsh` configured to automatically load function subdirectories
into your `$fpath`. This seems to be typical in most `zsh` setups.

    $ fpath=( ~/.zsh/functions/**/*(/N) $fpath )

Make sure the functions are being called from the `chpwd` function. If you don't
have `chpwd()` configured, you can use the included example.

    $ mv plugins/zsh-bundler-path-helpers/chpwd.example functions/chpwd
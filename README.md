# Bundler Path Helpers

This function will automatically add and remove bundled gems and binaries
to your `$GEM_PATH` and `$PATH` respectively. It is run immediately after
any command is executed .

## Conventions

* Your bundled gems must be stored in `vendor/bundle`
* You use `zsh`
* Your have a properly configured `$fpath`

## Installation

Go into your `zsh` dotfiles directory

    $ cd ~/.zsh

Clone the respository somewhere.

    $ git clone git://github.com/lordzork/zsh-bundler-path-helpers.git plugins/bundler-path-helpers

Alternatively, you can create a submodule.

    $ git submodule add git://github.com/lordzork/zsh-bundler-path-helpers.git plugins/bundler-path-helpers

Add the `functions` subdirectory to your `$fpath`. This should be done in your `.zshrc`.

    $ fpath+=$HOME/.zsh/plugins/*/functions/*(N)

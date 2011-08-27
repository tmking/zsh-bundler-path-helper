# Bundler Path Helpers

This function will automatically add and remove bundled gems and binaries
to your `$GEM_PATH` and `$PATH` respectively. It is run immediately
after the execution of any command.

## Conventions

* You use `zsh`
* Your have a properly configured `$fpath`

## Installation

Clone the respository somewhere.

    $ git clone git://github.com/lordzork/zsh-bundler-path-helpers.git ~/.zsh/plugins/bundler-path-helpers

Alternatively, you can create a submodule.

    $ git submodule add git://github.com/lordzork/zsh-bundler-path-helpers.git ~/.zsh/plugins/bundler-path-helpers

Add the `functions` subdirectory to your `$fpath`. This should be done in your `.zshrc`.

    $ fpath+=$HOME/.zsh/plugins/*/functions/*(N)

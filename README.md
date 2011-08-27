# Bundler Path Helper

`bundler-path-helper` is a Z shell function that will automatically add
and remove bundled gems and binaries to `$GEM_PATH` and `$PATH`
respectively. This means that you will no longer need to use `bundle exec`
when working on your project.

If the current bundle has gem collections for multiple ruby versions,
`bundler-path-helper` will attempt to guess the most appropriate version
based on the current ruby interpreter.

## Conventions

* You use `zsh`
* Your have a properly configured `$fpath`

## Installation

Clone the respository somewhere.

    $ git clone git://github.com/lordzork/zsh-bundler-path-helper.git ~/.zsh/plugins/bundler-path-helper

Alternatively, you can create a submodule.

    $ git submodule add git://github.com/lordzork/zsh-bundler-path-helper.git ~/.zsh/plugins/bundler-path-helper

Add the `functions` subdirectory to your `$fpath`. This should be done in your `.zshrc`.

    $ fpath+=$HOME/.zsh/plugins/*/functions/*(N)

## Notes

* `bundler-path-helper` should coexist peacefully with RVM since it only activates if the current directory's bundle was installed into a manually specified location.
* `bundler-path-helper` is run immediately after every command. It is lightweight enough that you shouldn't notice any additional lag.

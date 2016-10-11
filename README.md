# compare_migrations

Utility function to compare Rails migration files on a remote server against those locally. This is helpful for ascertaining which migrations will need to be run during a deploy.

## Conventions

* You use `zsh`
* You have a properly configured `$fpath` (more on this below)
* Your local source directory has the same name as the app directory on the remote server

## Installation

Clone the respository somewhere.

    $ git clone git://github.com/tmking/compare_migrations.git ~/.zsh/plugins/compare_migrations

Alternatively, you can create a submodule.

    $ git submodule add git://github.com/tking/compare_migrations.git ~/.zsh/plugins/compare_migrations

Add the `functions` subdirectory to your `$fpath`. This should be done in your `.zshrc`.

    $ fpath+=$HOME/.zsh/plugins/*/functions/*(N)

For tab completion to work, you'll need to add the Completion directory as well:

    $ fpath+=$HOME/.zsh/plugins/*/Completion/*(N)

## Usage

This plugin provides two commands, `compare_migrations` and `diff-remote`.

`compare_migrations <remote server>`

`diff-remote <remote server> <remote path> <local path>`

## Notes

`compare_migrations` will only work when you're inside of the source directory.

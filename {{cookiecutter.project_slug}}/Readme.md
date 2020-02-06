{{cookiecutter.project_name}}
=============================


{{cookiecutter.project_short_description}}


Configuration
----------

You probably want to edit `.stow-local-ignore`.  It already is configured to ignore the `.git` files as well as `Readme` and `Makefile`.   Use the `-n` option as in `stow -n -v --target="$HOME" -S .` to check which links will be created.  The `--adopt` option may also be useful.

**Makefile tricks**

- if you need to stow into multiple places you can add several lines like this

```
	stow -v --target="$$HOME/.vim/" -S config
```
I use this to stow vim config (in folder `config`) to both  `~/.vim` as well as `~/.config/nvim`.

The trick is also handy if you don't like working with hidden directories.



Installation
-------------

dotfiles can be copied in or being adopted using: `stow -v --target="$HOME" --adopt . `.

Use `make stow` to install the dotfiles.

Use `make install` to script installation of all necessary components.

Use `make update` for updates.


Further reading
---------------

`man stow`

`man git`

`man make`

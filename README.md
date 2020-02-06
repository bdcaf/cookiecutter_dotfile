dotfiles template
===========

[Cookiecutter](https://github.com/audreyr/cookiecutter) template for dotfile projects.  
These projects are generated that the actual files stay in the generated dotfile directory, and are
managed using [stow](https://www.gnu.org/software/stow/), which creates matching links in the target path (usually `$HOME`).


Requirements
------------
Install [`cookiecutter`](https://github.com/audreyr/cookiecutter) command line: `pip install cookiecutter`    

Usage
-----
Generate a new Cookiecutter template layout: `cookiecutter gh:bdcaf/cookiecutter_dotfile`.  See the generated Readme.md for further instructions.    

Tricks
------

**stow config**

- `stow-local-ignore` is essential to keep your documentation and other local files out of the config dir.
- `stowrc` allows to configure options for stow

**git config**
- `.gitignore` keeps temporary files out of git.
- `.gitkeep` is a hack so as git will not store empty directories - they may be empty as all files inside were ignored. They will miss in cloned repos and some software gives you errors due to this. Best to create as an empty file with `touch .gitkeep` in the correct location.

**Makefile tricks**

- Makefile uses `$` itself - so to work with environment variables you need to add another `$` - like the `$$HOME` in the default config.
- Makefile doesn't know about `~` - use `$$HOME` to point to it.
- if you need to stow into multiple places you can add several lines like this

```
	stow -v --target="$$HOME/.vim/" -S config
```
I use this to stow vim config (in folder `config`) to both  `~/.vim` as well as `~/.config/nvim`.

The trick is also handy if you don't like working with hidden directories.

**a little warning**
`make` runs commands in the `Makefile`. Spend a little time familiarizing you with the code in there - bad people might hide malicious code in there. It could also be abused to exfiltrate data.

License
-------
This project is licensed under the terms of the [MIT License](/LICENSE)

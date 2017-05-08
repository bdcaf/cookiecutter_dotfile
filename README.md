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

License
-------
This project is licensed under the terms of the [MIT License](/LICENSE)

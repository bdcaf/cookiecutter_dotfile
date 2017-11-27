dotfiles template
===========

[Cookiecutter](https://github.com/audreyr/cookiecutter) template for dotfile projects.  
These projects are generated that the actual files stay in the generated dotfile directory, and are
managed using [stow](https://www.gnu.org/software/stow/), which creates matching links in the target path (usually `$HOME`).

News
------

I am learning more and more about the R package workflow.  Combining this *and* a Make based workflow seems a waste.  I start the package [vignetteEngineMake](https://github.com/bdcaf/vignetteEngineMake) to bring make based vignettes to R packages.   Watch this for future developments.

Requirements
------------
Install [`cookiecutter`](https://github.com/audreyr/cookiecutter) command line: `pip install cookiecutter`    

Usage
-----
Generate a new Cookiecutter template layout: `cookiecutter gh:bdcaf/cookiecutter_dotfile`.  See the generated Readme.md for further instructions.    

License
-------
This project is licensed under the terms of the [MIT License](/LICENSE)

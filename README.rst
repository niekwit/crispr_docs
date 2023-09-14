
crispr_docs
============

CRISPR-Cas screening documentation


Creation of Github repository to store website code
----------------------------------------------------

Created empty repository named `crispr-docs`.

Cloned this repository on local computer:

```
$ git clone git@github.com:niekwit/crispr_docs.git
```

Building documentation using Sphinx (Python Documentation Generator)
---------------------------------------------------------------------

https://www.sphinx-doc.org/en/master/index.html

Created new conda env
``` 
$ mamba create -n crispr-docs  python=3.9 sphinx=7.2.5 sphinx_rtd_theme=1.3.0
$ mamba activate crispr-docs
```

Created source directory and conf.py
```
 $ cd /home/niek/Dropbox/scripts/crispr-docs
 $ sphinx-quickstart
Welcome to the Sphinx 7.2.5 quickstart utility.

Please enter values for the following settings (just press Enter to
accept a default value, if one is given in brackets).

Selected root path: .

You have two options for placing the build directory for Sphinx output.
Either, you use a directory "_build" within the root path, or you separate
"source" and "build" directories within the root path.
> Separate source and build directories (y/n) [n]: 

The project name will occur in several places in the built documentation.
> Project name: crispr-docs
> Author name(s): Niek Wit
> Project release []: 0.1

If the documents are to be written in a language other than English,
you can select a language here by its language code. Sphinx will then
translate text that it generates into that language.

For a list of supported codes, see
https://www.sphinx-doc.org/en/master/usage/configuration.html#confval-language.
> Project language [en]: 

Creating file /mnt/4TB_SSD/Dropbox (Cambridge University)/scripts/crispr_docs/conf.py.
Creating file /mnt/4TB_SSD/Dropbox (Cambridge University)/scripts/crispr_docs/index.rst.
Creating file /mnt/4TB_SSD/Dropbox (Cambridge University)/scripts/crispr_docs/Makefile.
Creating file /mnt/4TB_SSD/Dropbox (Cambridge University)/scripts/crispr_docs/make.bat.

Finished: An initial directory structure has been created.

You should now populate your master file /mnt/4TB_SSD/Dropbox (Cambridge University)/scripts/crispr_docs/index.rst and create other documentation
source files. Use the Makefile to build the docs, like so:
   make builder
where "builder" is one of the supported builders, e.g. html, latex or linkcheck.


```

Test documentation
-------------------

To test documentation, run the below command and open `index.html` in the test_docs directory:

```
$ sphinx-build -b html . test_docs/
```

Creating website using Readthedocs
-----------------------------------

https://readthedocs.org/

Created account and linked Github account.

Created `.readthedocs.yaml` and `requirement.txt`, and added relevant information (https://docs.readthedocs.io/en/stable/config-file/v2.html)



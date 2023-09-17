====================
Web site creation
====================

CRISPR-Cas screening documentation


Creation of Github repository to store website code
----------------------------------------------------

Created empty repository named `crispr-docs`.

Cloned this repository on local computer:

.. code-block:: console

   $ git clone git@github.com:niekwit/crispr_docs.git


Building documentation using Sphinx (Python Documentation Generator)
---------------------------------------------------------------------

https://www.sphinx-doc.org/en/master/index.html

Created new Conda environment

.. code-block:: console

   $ mamba create -n crispr-docs  python=3.9 sphinx=7.2.5 sphinx_rtd_theme=1.3.0
   $ mamba activate crispr-docs


Inititated Sphinx documentation

.. code-block:: console

 $ cd /home/niek/Dropbox/scripts/crispr-docs
 $ sphinx-quickstart
   

Test documentation
-------------------

To test documentation, run the below command and open `index.html` in the test_docs directory:

.. code-block:: console

   $ sphinx-build -b html . test_docs/


Creating website using Readthedocs
-----------------------------------

https://readthedocs.org/

Created account and linked Github account.

Created `.readthedocs.yaml` and `requirement.txt`, and added relevant information (https://docs.readthedocs.io/en/stable/config-file/v2.html)


`.readthedocs.yaml`:

.. code-block:: yaml

   # Read the Docs configuration file for Sphinx projects
   # See https://docs.readthedocs.io/en/stable/config-file/v2.html for details

   # Required
   version: 2

   # Set the OS, Python version and other tools you might need
   build:
   os: ubuntu-22.04
   tools:
      python: "3.9"

   # Build documentation in the "docs/" directory with Sphinx
   sphinx:
   configuration: conf.py
   # You can configure Sphinx to use a different builder, for instance use the dirhtml builder for simpler URLs
   # builder: "dirhtml"
   # Fail on all warnings to avoid broken references
   # fail_on_warning: true

   # Optionally build your docs in additional formats such as PDF and ePub
   # formats:
   #    - pdf
   #    - epub

   # Optional but recommended, declare the Python requirements required
   # to build your documentation
   # See https://docs.readthedocs.io/en/stable/guides/reproducible-builds.html
   python:
   install:
      - requirements: requirements.txt

`requirements.txt`:

.. code-block:: 

   sphinx==7.2.5
   sphinx_rtd_theme==1.3.0




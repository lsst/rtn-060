.. image:: https://img.shields.io/badge/rtn--060-lsst.io-brightgreen.svg
   :target: https://rtn-060.lsst.io
.. image:: https://github.com/lsst/rtn-060/workflows/CI/badge.svg
   :target: https://github.com/lsst/rtn-060/actions/

################################################
Supporting Computational Science with Rubin LSST
################################################

RTN-060
=======

More than 100 people from institutions around the world participated in a virtual workshop, "Supporting Computational Science with Rubin LSST," on March 21-22, 2023. The workshop welcomed anyone involved in the process of turning LSST data into science, especially those requiring specific computational hardware or software. The meeting focused on science use cases with Rubin LSST, and how these might be paired with specific In-Kind contributed computing resources (Independent Data Access Centers and Scientific Processing Centers (IDACs and SPCs). The workshop was followed by a two-day technical discussion between members of the Rubin IDACs Coordination Group and Rubin Data Management, aimed at understanding how to meet the demand from the community use cases and identifying technical challenges.  In this report, we summarize the outcome of the scientific workshop and the technical discussion, and identify some of the next steps needed for continuing progress.

Links
=====

- Live drafts: https://rtn-060.lsst.io
- GitHub: https://github.com/lsst/rtn-060

Build
=====

This repository includes lsst-texmf_ as a Git submodule.
Clone this repository::

    git clone --recurse-submodules https://github.com/lsst/rtn-060

Compile the PDF::

    make

Clean built files::

    make clean

Updating acronyms
-----------------

A table of the technote's acronyms and their definitions are maintained in the ``acronyms.tex`` file, which is committed as part of this repository.
To update the acronyms table in ``acronyms.tex``::

    make acronyms.tex

*Note: this command requires that this repository was cloned as a submodule.*

The acronyms discovery code scans the LaTeX source for probable acronyms.
You can ensure that certain strings aren't treated as acronyms by adding them to the `skipacronyms.txt <./skipacronyms.txt>`_ file.

The lsst-texmf_ repository centrally maintains definitions for LSST acronyms.
You can also add new acronym definitions, or override the definitions of acronyms, by editing the `myacronyms.txt <./myacronyms.txt>`_ file.

Updating lsst-texmf
-------------------

`lsst-texmf`_ includes BibTeX files, the ``lsstdoc`` class file, and acronym definitions, among other essential tooling for LSST's LaTeX documentation projects.
To update to a newer version of `lsst-texmf`_, you can update the submodule in this repository::

   git submodule update --init --recursive

Commit, then push, the updated submodule.

.. _lsst-texmf: https://github.com/lsst/lsst-texmf

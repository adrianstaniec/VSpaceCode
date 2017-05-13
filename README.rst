==========
VSpaceCode
==========

» *Spacemacs-like keybindings for Visual Studio Code*

-----

.. contents:: **Table of Contents**

-----

Presentation
============

This project tries to mimic Spacemacs_ key bindings in VSCode_.

Heavy Spacemacs users have trained their muscle memory around the **mnemonic**
key bindings that Spacemacs provides, and usually they start missing them when
using other text editors. The goal of this project is to provide a configuration
that maps Spacemacs key bindings to VSCode functionalities. This will allow
users to continue using their muscle memory and and the mnemonics they know in
VSCode.

It is not possible to replicate the full Spacemacs experience within VScode, but
it is at least possible to map some key bindings to functions offering the same
features as Spacemacs does. For instance, :kbd:`SPC g s` in Spacemacs opens git
version control through Magit, so it make sense to map it to open the "Source
Control" view in VScode. A list of the currently remapped key bindings is
available in the `Keybindings`_ section.

The `Installation`_ can currently not be automated as it requires manual
interventions, and updates have also to be resolved manually. This project is
young and the direction it should take is not really clear yet. This is
discussed in `this issue`_. Feel free to participate in this discussion if you have
insightful ideas.

:Author: Fabien Dubosson
:License: MIT (See LICENSE_)

.. _Spacemacs: https://github.com/syl20bnr/spacemacs
.. _VSCode: https://github.com/Microsoft/vscode
.. _`this issue`: https://github.com/StreakyCobra/VSpaceCode/issues/1
.. _LICENSE: LICENSE


Installation
============

First you will have to install VSCodeVim_ in order to make VSCode_
vim-compliant. To do so, press :kbd:`Ctrl + P`, enter ``ext install vscodevim``
and then press :kbd:`Return`. You can then press the ``Install`` button, wait
for it to finish, and then ``Reload`` the editor by clicking the associated
button.

To set up VSpaceCode, simply merge the content of the `config.json`_ file with
your own settings. To do so, press :kbd:`Ctrl + Shift + P`, enter ``user
settings`` and then press :kbd:`Return`:

- If you don't have any VSCodeVim configuration yet, you can simply copy/paste
  the content of `config.json`_ (without the top-level brackets) somewhere into
  your ``settings.json``.

- If you already have some VSCodeVim configurations, you will have to manually
  copy/paste the parts of `config.json`_ into the corresponding
  ``vim.otherModesKeyBindingsNonRecursive`` section of your ``settings.json``.

In any case it is recommended to keep the configurations you take from here
grouped in your ``settings.json`` so you can easily update them by just
copy/pasting the relevant parts.

.. _VSCodeVim: https://github.com/VSCodeVim/Vim
.. _VSpaceCode: https://github.com/StreakyCobra/VSpaceCode
.. _`config.json`: config.json


Keybindings
===========

The following keybindings are currently configured:

============================  ========================================
Key bindings                  Description
============================  ========================================
:kbd:`SPC` :kbd:`SPC`         Show commands
:kbd:`SPC` :kbd:`TAB`         Next editor
:kbd:`SPC` :kbd:`1`           Focus first editor group
:kbd:`SPC` :kbd:`2`           Focus second editor group
:kbd:`SPC` :kbd:`3`           Focus third editor group
:kbd:`SPC` :kbd:`b` :kbd:`b`  Open file in project
:kbd:`SPC` :kbd:`b` :kbd:`d`  Close active editor
:kbd:`SPC` :kbd:`f` :kbd:`f`  Open file
:kbd:`SPC` :kbd:`f` :kbd:`r`  Open recent files/folders
:kbd:`SPC` :kbd:`f` :kbd:`s`  Save file
:kbd:`SPC` :kbd:`g` :kbd:`s`  Open source control
:kbd:`SPC` :kbd:`p` :kbd:`f`  Open file in project
:kbd:`SPC` :kbd:`q` :kbd:`f`  Close window
:kbd:`SPC` :kbd:`q` :kbd:`q`  Close window
============================  ========================================


Contributing
============

Contributions are welcome. Spacemacs has more than one thousand key bindings and
it is very probably that the contributors of this project are not using them
all. Feel free to open pull requests if you have some interesting mappings that
do not exist yet. Please try to make the following changes in a **single
commit**:

- Keep bindings sorted in `config.json`_
- Add the corresponding line in the `Keybindings`_ section of this README
- Include your name in the `Contributors`_ section of this README


Contributors
============

Thanks to the following people for sharing their configurations and contributing
to this project:

- `CodeFalling <https://github.com/CodeFalling>`_
- `li-xinyang <https://github.com/li-xinyang>`_
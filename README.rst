`FZF <https://github.com/junegunn/fzf>`_ Widgets for `Xonsh <http://xon.sh>`_
======================

.. image:: https://img.shields.io/badge/License-GPL%20v3-blue.svg
   :alt: License
   :target: http://www.gnu.org/licenses/gpl-3.0

.. image:: https://img.shields.io/pypi/v/nine.svg
   :alt: Pypi version
   :target: http://pypi.python.org/pypi/xontrib-fzf-widgets


This extension will add some fzf widgets to your xonsh shell that you can bind and use as follows:

.. figure:: https://raw.githubusercontent.com/shahinism/xontrib-fzf-widgets/master/docs/cast.gif
   :alt: Screencast

Current widgets
----------------

- **ssh:** Search in `/etc/ssh/ssh_config` or `~/.ssh/config` items and issue `ssh` command on the chosen item.
- **history insert** Search in all history entries and insert the chosen command to the prompt.
- **find file** Find one or more files in the current directory and its sub-directories.

How to use it
----------------

Install the package:

.. code-block:: sh

   pip install xontrib-fzf-widgets

Enable it by adding `fzf-widgets` to your `~/.xonshrc` file:

.. code-block:: python

    xontrib load fzf-widgets

And set your desired keybindings for each widget in `~/.xonshrc` file or set it to `None` to disable it:

.. code-block:: python

    $fzf_history_binding = Keys.ControlR
    $fzf_ssh_binding = Keys.ControlS
    $fzf_file_binding = Keys.ControlT

You can find the names of various keys here_ in ``python-prompt-toolkit``.

.. _here: https://github.com/jonathanslenders/python-prompt-toolkit/blob/master/prompt_toolkit/keys.py

History size can be limited by setting the `$fzf_history_size` variable.


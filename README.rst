Commandline Magic
=================

This module will present simplest mechanism for working with command line options and arguments.


Example of the usage bellow:

.. code-block:: python

    import cm
    from cm.options.path import base
    from cm.options.db import port, name


    port.type = int
    port.default = 10
    port.help = "Lolwat"
    base.help = "Base path"

    if __name__ == '__main__':
        cm.parse_command_line()

and try to run it ``$ python test.py --help``

.. code-block::

    List of available program options:
    Group "db"
        --db-port       Lolwat [default: "10"]
        --db-name


    Group "path"
        --path-base     Base path


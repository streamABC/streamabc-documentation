Logimporter
***********

The streamABC Logimporter sends logs from Icecast, Shoutcast and AIS servers to our streamABC_ infrastructure.
This is necessary to generate statistics for listeners, create AGMA log files and other statistical analyzations.

You can use Logimporter to directly stream log-data to streamABC ("tail-mode") and to send 
a single file at once.

Logimporter can work with log-files from the following streaming servers:

- Icecast
- Shoutcast 1
- Windows Media Server
- AIS

Installation
------------

The Logimporter comes as a single static binary that you can
use without further installation. Just download the file and 
make it executable.

Get in contact with streamABC support to get your installation files.

Logimporter is available for Linux, Windows, macOS and BSD.

Logimporter is controlled with command lines parameters. To get a list of all
parameters execute this:

.. code-block:: bash

    ./logimporter --help

Tail-Mode
---------

This is the most common use case. In this mode Logimporter works like Unix *tail* command.
New lines that are added to a file are parsed and sent to streamABC in real-time.
The program stays in foreground until you end it with CTRL-C.

.. code-block:: bash

    ./logimporter --dbuser=DBUSER --dbpass=DBPASS --dbname=DBNAME --dbhost=DBHOST --logtype=icecast ./logs/access.log

**Note:** All values for data access are provided by streamABC when you need it.

Some log-types like Shoutcast need additional parameters. For more information see below.

Single File Mode
----------------

In this mode Logimporter send the content of one file.
All parameters work as in tail-mode. You just need to omit the --tail flag.

.. code-block:: bash

    ./logimporter --dbuser=DBUSER --dbpass=DBPASS --dbname=DBNAME --dbhost=DBHOST --logtype=icecast ./logs/access.log

**Note:** All values for data access are provided by streamABC when you need it.

The program show the import progress and automatically ends if the file is finished.

.. _streamABC: https://streamabc.com/


----

For more information, please open a ticket: |helpdesk|

Vistit our company website: |www.quantum-cast.com|



.. |helpdesk| raw:: html

    <a href="https://streamabc.zammad.com" target="_blank">https://streamabc.zammad.com</a>


.. |www.quantum-cast.com| raw:: html

   <a href="https://www.quantum-cast.com/" target="_blank">www.quantum-cast.com</a>
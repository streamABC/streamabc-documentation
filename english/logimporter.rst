Logimporter
***********

The streamABC *Logimporter* sends logs from streaming servers to our streamABC_ infrastructure.
This is necessary to generate statistics for listeners, create AGMA log files and other statistical analyzations.

You can use *Logimporter* to stream logs to streamABC ("tail-mode") on the fly or to send the content of a single file at once.

*Logimporter* can work with log files from these streaming servers:

- Icecast
- Shoutcast 1
- Windows Media Server
- AIS (Ver. 7.x and 8.x)

Installation
------------

The *Logimporter* is shipped as a single static binary that can be
used without further installation. Just download the file, put it somewhere and 
make it executable.

Get in contact with streamABC support to get your installation files.

*Logimporter* is available in versions for Linux, Windows, macOS and BSD Unix.

The program is operated with command lines parameters. To get a list of all
parameters execute this:

.. code-block:: bash

    ./logimporter --help

Tail-Mode
---------

This is the most common use case. In this mode *Logimporter* works like Unix *tail* command.
Tail mode starts at the end of the file. All new lines that are added to a file are parsed and sent to streamABC in real-time. Any lines that still exist in the file once you start are not transmitted.
The program stays in foreground until you end it with CTRL-C. You can create a init.d or systemd start script to run it in background and control it.

.. code-block:: bash

    ./logimporter --dbuser=DBUSER --dbpass=DBPASS --dbname=DBNAME --dbhost=DBHOST --logtype=icecast --tail ./logs/access.log

**Note:** All values for data access are provided by streamABC when you need it.

Some log types like Shoutcast need additional parameters. For more information see below.

Single File Mode
----------------

In this mode *Logimporter* send the content of one file at once. It starts with the first line and process the file until
all lines are done.
All parameters work as in tail-mode. You just need to omit the `--tail` flag.

.. code-block:: bash

    ./logimporter --dbuser=DBUSER --dbpass=DBPASS --dbname=DBNAME --dbhost=DBHOST --logtype=icecast ./logs/access.log

**Note:** All values for data access are provided by streamABC when you need it.

The program shows the import progress and automatically stops if the end of the file is reached.

.. _streamABC: https://streamabc.com/

AIS Logtype
----------------

AIS logs access and session logs. Please always use session logs because only these log files contain information 
on session durations.

AIS uses a configurable log field layout. Logimporter tries to detect the current field definition by using 
the line prefixed with `#Fields:` that is included in every session log file.

If no field configuration can be found it uses a default. 


----

For more information, please open a ticket: |helpdesk|

Visit our company website: |www.quantum-cast.com|



.. |helpdesk| raw:: html

    <a href="https://streamabc.zammad.com" target="_blank">https://streamabc.zammad.com</a>


.. |www.quantum-cast.com| raw:: html

   <a href="https://www.quantum-cast.com/" target="_blank">www.quantum-cast.com</a>

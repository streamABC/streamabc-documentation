QuantumCast Skip API
******************

The QuantumCast Skip API controls skips in streams using dedicated URL GET parameters appended to a QuantumCast stream URL.

*Note:* The channel behind the stream URL has to be skip enabled in the QuantumCast console backend to make use of this Skip API. 

Example streamURL: http://sabc-test.stream.vip/qc/mp3-256/ (or https://sabc-test.stream.vip/qc/mp3-256/)

URL parameters
--------------

+------------------------+--------------------------------+-------------------------------------+
| Name                   | Explanation                    | Example                             |
+========================+================================+=====================================+
| sabcsid                | Uinique listener ID (UUID)     | fb3c7ba352e3                        |
+------------------------+--------------------------------+-------------------------------------+
| skip                   | Session-ID for actual listener | e1d4c7a3-cae1-4a74-a489-7b41648bd9e7|
|                        | or live for livestream         |                                     |
+------------------------+--------------------------------+-------------------------------------+
| skip2                  | Position-ID of last item       | 7648                                |
+------------------------+------------+-------------------+-------------------------------------+

The ``sabcsid`` paramter is mandantory. It has to be unique and always the same for a specific user. 

If you are working on a web player you can use our QuantumCast_ Javascript-SDK_ to generate this listener id and decorate an existing stream URL.
Q

Initial start of a skippable stream
-----------------------------------

Every listener session has to be started with an valid listener id parameter ``sabcsid`` like so:
http://sabc-test.stream.vip/qc/mp3-256/?sabcsid=fb3c7ba352e3

This starts a default live stream session but prepares our backend system to upcoming skips of this user.

Skip to next element
--------------------

Start a new listener session with the same stream url like before but add a valid ``skip`` and ``skip2`` paramter:
http://sabc-test.stream.vip/qc/mp3-256/?sabcsid=fb3c7ba352e3&skip=e1d4c7a3-cae1-4a74-a489-7b41648bd9e7&skip2=7648

This starts a a new user stream session starting with the next song after position defined with ``skip2``.

You get the required values for ``skip`` and ``skip2`` over a Websocket connection to our player services API as described here:
    
.. seealso:: `Websockets Documentation </en/latest/websockets.html>`_

With a subscription to ``/metadata/{listenerid}`` you get all metadata events in real-time.

If it's not possible to open a websockets connection in addition to the stream playback you can generate
your own session id and send this value as `skip` parameter and leave `skip2` blank. Bear in mind
that this comes with some drawbacks: A stream start without a valid session id from our QuantumCast backend will
result in slightly longer wait times until audio begins. In addition you can only skip to the next element in the playlist.

A websockets connection on the other hand gives you some more useful data. You get the users metadata (artist, song)
of the element playing right now and the next element as long as cover art and some status information.
You also get information about whether the actual element is an advertisement and how long it plays.

Tune back to live stream
------------------------

Start a new listener session with the same stream url like before but add `live` as `skip` parameter:
http://sabc-test.stream.vip/qc/mp3-256/?sabcsid=fb3c7ba352e3&skip=live

You can also just omit all skip parameters to start a livestream. But if the disconnect time is too short
our backend tries to re-connect you listener to his already running skip stream. A `skip=live` forces
a live stream start.


.. _QuantumCast: https://www.quantumcast-digital.com
.. _Javascript-SDK: https://github.com/streamABC/api-player


---

For more information, please open a ticket: |helpdesk|

Visit our company website: |www.quantumcast-digital.com|



.. |helpdesk| raw:: html

    <a href="https://streamabc.zammad.com" target="_blank">https://streamabc.zammad.com</a>


.. |www.quantumcast-digital.com| raw:: html

   <a href="https://www.quantumcast-digital.com/" target="_blank">www.quantumcast-digital.com</a>
   

streamABC Websockets
********************

This documentation describes the use of the low-level Websockets API. If possible use a higher-level
SDK that abstracts all steps. Currently this is only available for Javascript here:
https://github.com/streamABC/api-player

You find all detailed docs for transferred messages here:
https://github.com/streamABC/api-player/blob/master/Docs-Playerservices.md

The streamABC Websockets allows subscribing for meta-data events on streamABC_ audio streams.

Default URL endpoint for websockets services is:
``wss://playerservices.streamabc.net``

The websocket endpoint uses nes-Protocol_.

Metadata Events for Users Subscription
--------------------------------------

To receive meta-data events for individual users subscribe to this path:
``/metadata/{userid}``

*Note*: In order for this to work you have to decorate the stream-url with a GET parameter ``sabcsid={userid}`` and start streaming.

After subscribing the server publishes messages containing a JSON object as payload. 

Metadata Events for Channel Subscription
----------------------------------------

To receive meta-data events for specific channels subscribe to this path:
``/metachannel/{channelkey}``

Please use the channel key provided by streamABC.

Metadata Events for Station Subscription
----------------------------------------

To receive meta-data events for specific channels subscribe to this path:
``/metastation/{stationid}``

Please use the station-id provided by streamABC.


.. _streamABC: https://streamabc.com/
.. _nes-Protocol: https://github.com/hapijs/nes/blob/master/PROTOCOL.md

----

For more information, please open a ticket: |helpdesk|

Vistit our company website: |www.quantum-cast.com|



.. |helpdesk| raw:: html

    <a href="https://streamabc.zammad.com" target="_blank">https://streamabc.zammad.com</a>


.. |www.quantum-cast.com| raw:: html

   <a href="https://www.quantum-cast.com/" target="_blank">www.quantum-cast.com</a>
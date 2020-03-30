QuantumCast Websockets API
************************

This documentation describes the use of the low-level Websockets API as part of our PlayerServices API.

If possible use a higher-level SDK that abstracts all steps. Currently, a Javascript Version is available here:
https://github.com/streamABC/api-player

You find all detailed docs for transferred messages here:
https://github.com/streamABC/api-player/blob/master/Docs-Playerservices.md

The QuantumCast Websockets allows subscribing for meta-data events on QuantumCast_ audio streams.

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

Please use the channel key provided by QuantumCast.

Metadata Events for Station Subscription
----------------------------------------

To receive meta-data events for specific channels subscribe to this path:
``/metastation/{stationid}``

Please use the station-id provided by QuantumCast.


.. _QuantumCast: https://www.quantumcast-digital.com
.. _nes-Protocol: https://github.com/hapijs/nes/blob/master/PROTOCOL.md


----

For more information, please open a ticket: |helpdesk|

Visit our company website: |www.quantumcast-digital.com|



.. |helpdesk| raw:: html

    <a href="https://streamabc.zammad.com" target="_blank">https://streamabc.zammad.com</a>


.. |www.quantumcast-digital.com| raw:: html

   <a href="https://www.quantumcast-digital.com/" target="_blank">www.quantumcast-digital.com</a>
   

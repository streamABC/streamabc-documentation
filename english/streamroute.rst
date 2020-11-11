StreamRoute
***********

StreamRoute is a scalable and highly available system service for effectively connects user stream requests to Audiostreamer infrastructure running in QuantumCast. The service can be available with own custom domain and automatic https certification.

Features:

-	Generate listerner IDs if necessary, based on client fingerprinting
-	Responsible for aggregator detection 
-	Skip request specific handling
-	Alias domain when required
-	Forwarding parameters to QuantumCast-Audiostreamer or other Streamers
-	Detour blacklist-IPs
-	No pre-roll spot at specific aggregator requests, e.g. wake up alarm
-	Generate PLS and M3U-Playlists on request over stream URL
-	Create individual landing pages with metadata for aggregators
-	Certification for listeners from own infrastructure
-	GDPR no tracking option
-	Special handling for special aggregators


All communications with QuantumCast user audio streams comprises of a set of parameters that can be passed in the stream request. 
These parameters will capture sufficient details about the available opportunity and help serve a targeted audio stream to the user.

StreamRoute request will look similar to the one below:

https://domain/programm/format/aggregator/listenerId/?awparams

.. list-table:: StreamRoute Request Parameters
   :widths: 25 25 50
   :header-rows: 1

   * - Name
     - Description
     - Example
   * - awparams
     - awparams are passed to certain players / aggregators
     - amsparams=playerid:tunein;skey:1605116562



.. _QuantumCast: https://www.quantumcast-digital.com
.. _nes-Protocol: https://github.com/hapijs/nes/blob/master/PROTOCOL.md


----

For more information, please open a ticket: |helpdesk|

Visit our company website: |www.quantumcast-digital.com|



.. |helpdesk| raw:: html

    <a href="https://streamabc.zammad.com" target="_blank">https://streamabc.zammad.com</a>


.. |www.quantumcast-digital.com| raw:: html

   <a href="https://www.quantumcast-digital.com/" target="_blank">www.quantumcast-digital.com</a>
   

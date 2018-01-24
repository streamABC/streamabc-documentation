.. index:: StreamURLs

StreamURLs
***********

StreamURLs und deren Verbreitungskanäle bilden in Streaming-Infrastrukturen die wichtigste Schnittstelle für die Verbreitung digitaler Radio-Kanäle im Netz.

Ihnen gilt ganz besondere Aufmerksamkeit. Ihre Systematisierung ist wichtig und spielt gerade beim Betrieb von sehr vielen Audiostreams eine große Rolle.

Um so mehr Verbreitung die StreamURL durch Aggregatoren wie z.B. TuneIn, radio.de, etc. erfahren, desto größer ist die sogenannte `technische Reichweite <https://de.wikipedia.org/wiki/Technische_Reichweite>`_ des Streams.
Es gilt, je mehr Verbreitung die StreamURL erfährt, desto mehr Personen werden den Stream hören können.
Eigene Apps und Websites erhöhen auch die technische Reichweite.


----

.. index:: StreamURLs Schema
.. index:: Aufbau StreamURLs

Nach welchem Schema sind die StreamURLs aufgebaut?
--------------------------------------------------
Es erfolgt eine Systematisierung der StreamURLs nach folgendem Schema:

`http://domain/programm/format/`


----

.. index:: StreamURLs & Aggreagtoren
.. index:: Aggreagtoren messen

Wie ist es möglich mit der StreamURL die jeweiligen Reichweiten von Homepage, Apps und Aggreagtoren zu messen?
--------------------------------------------------------------------------------------------------------------
Um zu messen, wieviel Hörer den Stream z.B. über die Homepage hören, dafür muss an die StreamURL lediglich das Wort 'Homepage' angehangen werden und auf der Homepage verlinkt werden..

z.B. 

\http://domain/programm/format/**Homepage/**

Das Gleiche gilt auch für jeden anderen Aggreagtor. Zum Beispiel in der App diese URL nutzen:

\http://domain/programm/format/**App/**

oder an TuneIn diese StreamURL weitergeben:

\http://domain/programm/format/**Tunein/**


----

.. index:: Https-StreamURLs

Ist Https für die StreamURLs und Audiostreams verfügbar?
--------------------------------------------------------
Ja, für alle Streams ist https aktiviert.


----

.. index:: individuelle StreamURL-Domain
.. index:: DNS-Eintrag für StreamURL-Domain

Ist es möglich eine eigene Domain für die StreamURLs zu nutzen?
---------------------------------------------------------------
Ja. Es ist möglich, eine individuelle StreamURL-Domain eintragen zu lassen.
Dafür bitte innerhalb der Console den Bereich "StreamURLs" -> "Domain hinzufügen / löschen" aufrufen.
Unter "System StreamURL-Domänen" finden Sie ihrer aktuell eingerichtete StreamURL-Domain.

Sie müssen nun im DNS für die gewünschte Domain einen CNAME auf ihrer aktuell eingerichtete StreamURL-Domain einrichten:
z.B. 
    streams.meine-domain.de IN CNAME  {system-name}.stream.vip.

Anschließend uns kurz Bescheid geben. Dafür bitte ein Ticket öffnen: https://streamabc.zammad.com

Wir schalten dann ihre individuelle StreamURL-Domain frei.


----

Bei weiteren Fragen bitte ein Ticket öffnen: |helpdesk|

Besuchen Sie unsere Unternehmens-Website |www.streamabc.com|



.. |helpdesk| raw:: html

    <a href="https://streamabc.zammad.com" target="_blank">https://streamabc.zammad.com</a>


.. |www.streamabc.com| raw:: html

   <a href="https://www.streamabc.com/#quantum-cast" target="_blank">www.streamabc.com/#quantum-cast</a>
   

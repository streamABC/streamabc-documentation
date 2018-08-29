.. index:: Werbung

Werbung
***********

.. index:: Werbeformen
.. index:: Werbeeinblendung Typen
.. index:: Pre-Stream Audio Ad
.. index:: Preroll Audio Ad
.. index:: In-Stream Audio Ad

Welche Formen der automatischen Werbeeinblendung gibt es?
---------------------------------------------------------
Es gibt zwei Arten der automatischen Werbeeinblendung:

Pre-Stream Audio Ad
    Beim Start des Streams wird Werbung zu hörer sein

In-Stream Audio Ad 
    Mitten im Stream können Werbeblöcke eingeblendet werden. Der genaue Zeitpunkt der Werbeeinblendung wird vom Programmanbieter ausgelöst.


----

.. index:: Werbeeinblendung Funktionsweise

Wie funktioniert die automatische Werbeeinblendung?
---------------------------------------------------
Mit Start des Streams oder mit Auslösen des Werbeimpulses (Trigger) fragt das Streamingsystem bei Ihrem Vermarkter an, ob für diesen Hörer ein Spot vorliegt. Wenn der Vermarkter eine positive Antwort gibt, dann wird der Stream kurz angehalten und das Streamingsystem blendet automatisch einen Spot in ihrem Stream ein. Gleichzeitig wird automatischen ein Protokoll über die Werbeeinblendung erstellt und an ihren Vermarkter versendet.
Mit der Spot-Anfrage für jeden Hörer beim Vermarkter muss eine ZonenID mit übergeben werden. Diese ZonenIDs für Pre-Stream und In-Stream erhalten Sie von Ihrem Vermarkter 


----

.. index:: DAAST-Schnittstelle 
.. index:: Digital Audio Ad Serving Template

Warum nutzen wir für die Werbeeinblendung die DAAST-Schnittstelle?
---------------------------------------------------
Mit Hilfe der `DAAST-Schnittstelle <https://www.iab.com/guidelines/digital-audio-ad-serving-template/>`_ 
ist es möglich erweiterte Premium-Leistungen bei der Werbeauslieferung anbieten zu können.

- Echtzeit-Monitoring und Überwachung
- Werbeauslieferung bei skippable Radiostreaming
- Werbeauslieferung bei personalisiertem Audiostreaming
- Zugang zum Markt der Audio-Adserver
- Automatische Konfiguration der Werbeeinblendung
- Self-Service-Portal für Echtzeitanpassungen der Werbungblöcke
- Entwicklung neuer Werbeformen
- Eigenwerbespots ohne Audio-Adserver-Kosten


Klassische Werbeeinblendungen für Audio-Livestreaming, wie. z.B. Prerollspots oder alle Formen der Instream-Werbeeinblendung werden selbstverständlich auch über die DAAST-Schnittstelle angeboten.

Weitere Informationen zur DAAST-Schnittstelle finden Sie bei der IAB unter:
`https://www.iab.com/guidelines/digital-audio-ad-serving-template/ <https://www.iab.com/guidelines/digital-audio-ad-serving-template/>`_


----

.. index:: Werbeeinblendung Voraussetzungen
.. index:: Ad-ZonenID
.. index:: ZonenID
.. index:: DAAST-Schnittstelle 

Welche Voraussetzung müssen für eine automatische Werbeeinblendung vorhanden sein?
----------------------------------------------------------------------------------
Sie benötigen einen kompatiblen Vermarkter. Mit folgenden Audio-Vermarktern arbeiten wir zur Zeit:
`RMS <http://www.rms.de>`_, `Spotcom <http://www.spotcom.de>`_, `STUDIO GONG <https://www.studio-gong.de/>`_

Basis für die Zusammenarbeit ist das `Adswizz-Ad-System <http://www.adswizz.com/>`__ und die `DAAST-Schnittstelle <https://www.iab.com/guidelines/digital-audio-ad-serving-template/>`_.

Für Pre-Stream Audio Ad ist nur die Pre-Stream-ZonenID notwendig. 
Für In-Stream Audio Ad benötigen Sie auch eine ZonenID. Zusätzlich aber muss ein Werbeimpuls noch erfolgen, damit das Streamingsystem den Spot zum richtigen Zeitpunkt in den Stream einblendet. 

----

.. index:: In-Stream Audio Ad / Auslöser
.. index:: In-Stream Audio Ad mittels Beep
.. index:: In-Stream Audio Ad mittels Metadaten

Wie wird In-Stream Audio Ad ausgelöst?
--------------------------------------
Ein In-Stream Audiospot wird durch einen Werbeimpuls ausgelöst.
Dieser Werbeimpuls kann auf zwei Wegen erfolgen:

Beep
    Sie können in ihrem Audiosiganl einen speziellen Ton verstecken (Beep). Das Streamingsystem erkennt diesen Ton (Beeperkennung) und startet zu diesem Zeitpunkt die automatische Werbeeinblendung.

Metadaten
    In einen Audio-Stream können Metadaten integriert werden. Es ist möglich für das Streamingsystem bei einem bestimmten Muster der Metadaten die automatische Werbeeinblendung zu starten. 

----

.. index:: Capping
.. index:: Pre-Stream Audio Ad Capping

Wie kann ich das Capping für Pre-Stream Ads beeinflussen?
---------------------------------------------------------
Für ein korrektes Capping muss der Ad-Server den Hörer zuverlässig wiedererkennen können. Nur dann kann er das Ausspielen der Spots über die Hörersession beeinflussen.
Standardmäßig erzeugt unser Streamingsystem einen Hash-Wert über verschiedene Parameter der Verbindung wie IP-Adresse, User-Agent, Referrer usw. Da viele Clients jedoch auch aus Datenschutzgründen nur wenige Daten senden und die IP-Adresse in größeren Netzen nicht mehrfach verwendet wird,
ist dieser Hash-Wert für korrektes Capping meist nicht ausreichend.

Die Player als Website oder App haben meist mehr Möglichkeiten, den Hörer individuell zu identifizieren. So kann im Player ein Cookie verwendet werden oder in Apps eine eindeutige Gerätekennung.
Die Hörer-ID kann ein alphanumerischer Wert sein. Sonderzeichen müssen URL-codiert werden.
Diese eindeutige Hörer-ID kann über die StreamURL als PATH-Parameter oder GET-Parameter übergeben werden:

Als Path-Parameter:
`http://domain/programm/format/aggregator/hoerer-id`

Als GET-Parameter:
`http://domain/programm/format/?sabcsid=hoerer-id`

.. seealso:: `Schema StreamURLs </de/latest/streamurls.html#nach-welchem-schema-sind-die-streamurls-aufgebaut>`_

Die Hörer-ID wird dann vom Streamingsystem bei Ad-Requests automatisch an den Ad-Server weitergeleitet.

----

Bei weiteren Fragen bitte ein Ticket öffnen: |helpdesk|

Besuchen Sie unsere Unternehmens-Website |www.streamabc.com|



.. |helpdesk| raw:: html

    <a href="https://streamabc.zammad.com" target="_blank">https://streamabc.zammad.com</a>


.. |www.streamabc.com| raw:: html

   <a href="https://www.streamabc.com/#quantum-cast" target="_blank">www.streamabc.com/#quantum-cast</a>
   
Werbung
***********




Welche Formen der automatischen Werbeeinblendung gibt es?
------------------------------------------------------------
Es gibt zwei Arten der automatischen Werbeeinblendung:

- Pre-Stream Audio Ad
    Beim Start des Streams wird Werbung zu hörer sein

- In-Stream Audio Ad 
    Mitten im Stream können Werbeblöcke eingeblendet werden. Der genaue Zeitpunkt der Werbeeinblendung wird vom Programmanbieter ausgelöst.




Wie funktioniert die automatische Werbeeinblendung?
------------------------------------------------------------
Mit Start des Streams oder mit Auslösen des Werbeimpulses (Trigger) fragt das Streamingsystem bei Ihrem Vermarkter an, ob für diesen Hörer ein Spot vorliegt. Wenn der Vermarkter eine positive Antwort gibt, dann wird der Stream kurz angehalten und das Streamingsystem blendet automatisch einen Spot in ihrem Stream ein. Gleichzeitig wird automatischen ein Protokoll über die Werbeeinblendung erstellt und an ihren Vermarkter versendet.
Mit der Spot-Anfrage für jeden Hörer beim Vermarkter muss eine ZonenID mit übergeben werden. Diese ZonenIDs für Pre-Stream und In-Stream erhalten Sie von Ihrem Vermarkter 


Welche Voraussetzung müssen für eine automatische Werbeeinblendung vorhanden sein?
------------------------------------------------------------
Sie benötigen einen kompatiblen Vermarkter. Mit folgenden Audio-Vermarktern arbeiten wir zur Zeit:
`RMS <http://www.rms.de>`_, `Spotcom <http://www.spotcom.de>`_

Basis für die Zusammenarbeit ist das `Adswizz-Ad-System <http://www.adswizz.com/>`_ und die `DAAST-Schnittstelle <https://www.iab.com/guidelines/digital-audio-ad-serving-template/>`_.

Für Pre-Stream Audio Ad ist nur die Pre-Stream-ZonenID notwendig. 
Für In-Stream Audio Ad benötigen Sie auch eine ZonenID. Zusätzlich aber muss ein Werbeimpuls noch erfolgen, damit das Streamingsystem den Spot zum richtigen Zeitpunkt in den Stream einblendet. 


Wie wird In-Stream Audio Ad ausgelöst?
------------------------------------------------------------
Ein In-Stream Audiospot wird durch einen Werbeimpuls ausgelöst.
Dieser Werbeimpuls kann auf zwei Wegen erfolgen:

- Beep
    Sie können in ihrem Audiosiganl einen speziellen Ton verstecken (Beep). Das Streamingsystem erkennt diesen Ton (Beeperkennung) und startet zu diesem Zeitpunkt die automatische Werbeeinblendung.

- Metadaten
    In einen Audio-Stream können Metadaten integriert werden. Es ist möglich für das Streamingsystem bei einem bestimmten Muster der Metadaten die automatische Werbeeinblendung zu starten. 




.. |www.streamabc.com| raw:: html

   <a href="https://www.streamabc.com" target="_blank">www.streamabc.com</a>
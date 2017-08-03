Metadaten
***********



Was muss beachtet werden bei Metadaten und Instream-Werbung?
------------------------------------------------------------
Wird für die Werbezeit ein Musikbett/Filler im Stream eingeplant, dann muss bei den Metadaten nichts weiter beachtet werden.

Sollte aber für die Werbeeinblendung der Stream angehalten werden, so gilt es folgende Besonderheit zu berücksichtigen.
Jedem Hörer werden individuelle Spots mit unterschiedlicher Spieldauer ausgeliefert. Somit verändert sich auch für jeden Hörer individuell der Versatz zum Programmstream und dessen Metadaten. 
Um weiterhin eine syncrone Metadatenanzeige im Player zu haben, muss der Player die Metadaten aus dem Stream auslesen.
Klassiche WLan-Radios haben damit kein Problem. Auch Apps können die Metadaten aus dem Stream direkt auslesen, aber diese Funktion muss speziell aktiviert werden.
Aber Webplayer im Browser können das nicht.
Für Internet-Browser muss eine spezielle Schnittstelle zum Stremingserver implementiert werden, welche für jeden Hörer individuell die Metadaten ermittelt und überträgt.

Innerhalb der streamABC-Infrastruktur kann dafür ein spezieller Playerservice genutzt werden.

- `Documentation for streamABC player API <https://github.com/streamABC/api-player/blob/master/Docs-Playerservices.md>`_



.. _streamABC: https://streamabc.com/
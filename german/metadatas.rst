Metadaten
***********


Wo kann man die Metadaten-Injektion konfigurieren?
--------------------------------------------------
Bei einem Livestream von eigener Audioquelle ist es meist gewünscht, aktuelle Infos zum Inhalt mit in den Stream zu packen.
Diese Metadaten müssen dann in den Livestream injiziert werden.
Die Übermittlung von Metadaten erfolgt über einem HTTP-Push.
Die URL für den HTTP-Push erhalten Sie übergansweise noch manuell.
Dafür bitte ein Ticket öffnen: https://streamabc.zammad.com

Ein Upgrade ist bereits in Arbeit. 
Anschließend wird es in der Console ein Menüpunkt "Metadaten" geben. 
Dort kann man dann die URL erfahren.


Wie kann man aktuelle Metadaten übermitteln?
--------------------------------------------
Für die Übermittlung der aktuellen Metadaten mittels HTTP-Push erhalten Sie pro Channel einen HTTP-Endpoint mit folgender Schnittstellenspezifikation:


1.)     Übergabe folgender Daten per GET-Parameter:
    a.  song={URL-Encodierter String zum Titel}
    b.  artist={URL-Encodierter String zum Artist}
    c.  duration={Ganzzahliger Wert entspricht der Titellänge in Sekunden}
    d.  time={Ganzzahliger Wert entspricht dem Zeitpunkt des Starts als Timestamp}
    e.  separator={URL-Encodiertes Zeichen inkl. Leerzeichen für Abstand zu Artist und Song}

2.)     Die Parameter song, artist, duration, time müssen zwingend übergeben werden. Das Parameter separator ist optional.
    Alle Parameter müssen URL-encodiert übergeben werden.

3.)     Parameter song
    a.  Angabe der Titels als URL-encodierter String (Alle Sonderzeichen sind erlaubt)
    b.  Wert ‚false‘ ist erlaubt. In diesem Fall wird der Separator ignoriert und nur das Parameter artist verwendet. Das Parameter artist darf nicht auch ‚false‘ sein.

4.)     Parameter artist
    a.  Angabe des Artisten als URL-encodierter String (Alle Sonderzeichen sind erlaubt)
    b.  Wert ‚false‘ ist erlaubt. In diesem Fall wird der Separator ignoriert und nur das Parameter song verwendet. Das Parameter song darf nicht auch ‚false‘ sein.

5.)     Parameter duration
    a.  Angabe der Titellänge in Sekunden als ganzzahliger Wert. Der Wert muss größer 0 sein.
    b.  Wert ‚null‘ erlaubt. In diesem Fall wird der Fallback deaktiviert. Die übergebenen Metadaten bleiben damit auf unbestimmte Zeit aktiv und werden nicht mehr automatisch auf den Fallback zurückgesetzt. Erst mit dem nächsten Senden neuer Metadaten kann dieser Status aufgehoben werden.

6.)     Parameter time
    a.  Angabe des Zeitpunkts des Titelstarts als ganzzahliger Timestamp-Wert
    b.  Der Wert muss ein gültiger Timestamp-Wert sein.

7.)     Parameter seperator
    a.  Möglichkeit der Angabe des Trennerzeichens zwischen Artist und Song. Das Parameter ist optional.
    b.  Der Wert muss als URL-encodierter String übergeben werden. Auch die Leerzeichen für den gewünschten Abstand zu Artist und Song müssen enthalten sein.
    c.  Sollte das Parameter seperator nicht mit übergeben werden, so wird automatisch dieser Wert gesetzt „ - “.

8.)     Fehler     
    HTTP-Requests, welche aufgrund von Fehlern in den übergebenen Daten fehlschlagen, werden mit HTTP/501 ‚malformed/invalid field data‘ beantwortet.





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
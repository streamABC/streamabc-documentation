Audioquelle
***********



Welche muss man beim Neuanlegen einer Audioquelle beachten?
-----------------------------------------------------------
Sie möchten einen neuen Channel anlegen und mit einer eigenen Audiosignal beliefern. 
Dann sind folgende Dinge zu beachten:

-   Legen Sie eine neue Audioquelle in der Console an.
-   Die konfigurierten Eigenschaften der Audioquelle in der Console (Bitrate, Codec, SR und M/S) müssen mit den Einstellungen in ihrem Encoder übereinstimmen.
-   Liefern Sie mit einer möglichst hohen Qualität an.


----

In welcher Form können Sie das Audiosignal zuliefern?
------------------------------------------------------------
Sie können uns ihr Audiosignal gern als MP3 anliefern. 
Die ideale Audioquelle hat folgende Eigenschaften:

- Codec: MP3
- Bitrate: 192kbps oder größer (konstante Bitrate, CBR)
- Samplerate: 44,1kHz
- Audiokanäle: Stereo



----

Sie möchten kein Transcoding, und die perfekte Audioquelle direkt anliefern. Wie konfiguriert man das?
------------------------------------------------------------------------------------------------------
Das ist ganz einfach. Man muss dazu nur wissen, dass bei gleichen Eigenschaften von Audioquelle und Hörer-Mountpoint kein Transcoding gestartet wird.

1.  In der Console unter "Audioquelle" eine neue Audioquelle anlegen. 
    Dabei unbedingt auf die korrekte Konfiguration achten: Bitrate, Codec, SR und M/S


2.  In der Console unter "Hörer-Mountpoints" ein neuen Hörer-Mountpoint erstellen.
    Dabei die eben angelegte Audioquelle auswählen und bei Bitrate, Codec, SR und M/S die gleichen Einstellungen wie bei der Audioquelle verwenden.
    Das System erkennt dann automatisch, dass die Eigenschaften von Audioquelle und Hörer-Mountpoint identisch sind. 
    Bei gleichen Eigenschaften von Audioquelle und Hörer-Mountpoint wird kein Transcoding durchgeführt.
    In der Spalte "Transcoding" erscheint dann bei diesem Hörermount ein Strich (-).

3.  Abschließend nicht vergessen unter "StreamURLs" den neuen Hörermount als Ziel-Mount zu konfigurieren  

----

Besuchen Sie unsere Unternehmens-Website |www.streamabc.com|

.. |www.streamabc.com| raw:: html

   <a href="https://www.streamabc.com/#quantum-cast" target="_blank">www.streamabc.com/#quantum-cast</a>
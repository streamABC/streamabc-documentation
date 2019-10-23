.. index:: channelservices

Channelservices
****************


----

.. index:: Einen neuen Channel erstellen mit Hilfe des PlaylistDesigners
.. index:: Symbole / Icons
.. index:: Die Hörerzahlen auf einen Blick

Einen neuen Channel erstellen mit Hilfe des PlaylistDesigners
==============================================================

Unter „Channelservices“ auf „Neu anlegen“ klicken und anschließen den Namen des Channels, die ProgrammmarkenID und die Audioquelle definieren. 

.. image:: img/PD_Channel_neu_anlegen.png

Die ProgrammmarkenID ist für jeden Nutzer vorgegeben. Sollte eine neue benötigt werden, können Sie sich an unseren Support wenden.

Die Audioquelle richtet sich danach, ob der Stream mit dem QuantumCast PlaylistDesigner erstellt wurde oder ob eine Audioquelle zugeliefert werden soll. Im Beispiel nutzen wir den PlaylistDesigner. Anschließend auf „Erstellen“ klicken und fertig.

Nun kann man das Setup des Channels einstellen. Wichtig: jede Eingabe mit einem Klick auf den Haken bestätigen.

.. image:: img/PD_Setup_Channel.png

Die Angaben von Kurzname, Claim, Standort, Sprache, Genre etc. sind optional, helfen aber bei der Zulieferung an Aggregatoren und Vermarkter. Zur Finalisierung auf „Konfiguration jetzt veröffentlichen“ gehen und der Channel ist erstellt.

.. image:: img/PD_Konfiguration_veroeffentlichen.png

Nun muss das Playout für den Channel eingerichtet werden. Dafür im Menü „Playout“ anwählen und auf „+ Neues Playout aktivieren“ klicken.

.. image:: img/PD_Playout.png

Dann kann man die Quelle und die Ausgabe-Qualität einstellen. Die Quelle ist hierbei eine im PlaylistDesigner erstellte und abgespeicherte Playlist bzw. ein Smartblock. Die Ausgabe-Qualität enthält automatisch eine Voreinstellung (siehe unten) - mit einem Klick darauf, können aber weitere Einstellungen getroffen werden. Am Ende auf „speichern & beauftragen“ gehen. Achtung: dies kann einige Sekunden dauern. Bitte warten bis der Prozess beendet ist.

.. image:: img/PD_Playout_einstellen.png

Wurde das Playout erfolgreich gespeichert, kann man noch weitere Modifikationen vornehmen. In der Grundeinstellung ist als Playout-Typ „Basic“ eingestellt - der Funktionsumfang ist auf Basis-Funktionalitäten begrenzt. Für professionelle Online-Audio-Produzenten empfiehlt sich die Einstellung „Professional“.

.. image:: img/PD_Playout_Typ_einstellen.png

Den Unterschied machen Funktionen, wie z.B. die individuelle Einstellung des Mixing und Soundprocessing aus. Die Nutzung von „Stereo Tool“ ist ebenfalls ein Teil des „Professional“-Playout. In der „Basic“-Version sind diese Möglichkeiten deaktiviert.

.. image:: img/PD_Playout_Typ_Basic.png

Sobald man sich für „Professional“ entscheidet, wird der erweiterte Funktionsumfang freigeschaltet - die Abrechnung erfolgt automatisch.

.. image:: img/PD_Playout_Typ_Professional.png

.. seealso:: `Video-Tutorial "StartNext" <https://www.youtube.com/watch?v=PuMSmgWzTe4>`_

Achtung! In unserem Beispiel ist die Anzahl der Titel „0“. Das bedeutet in diesem Fall nicht, dass keine Elemente in der Liste vorhanden sind, sondern es handelt sich um einen „Dynamischen Smartblock“. Da in diesem Fall die Längen variieren, weil die Abfolge automatisch immer neu erstellt wird, kann die Titelanzeige in diesem Fall kein eindeutiges Ergebnis liefern. Bei „Playlisten“ und „statischen Smartblöcken“ wird aber die korrekte Titelanzahl angezeigt.

Um etwas hören zu können, wie nun noch eine streamURL benötigt. 

.. image:: img/PD_Channel_StreamURL_Einstellung.png

Dafür in den Bereich „StreamURLs“ gehen und in der Spalte „Wert“ eine Domain auswählen und einen StreamURL-Key festlegen. Anschließend auf „Konfiguration jetzt veröffentlichen“ klicken. Dann erstellen sich automatisch die StreamURLs entsprechend der vorher definierten „Ausgabe-Qualität“.

Unter „Test & Kontrolle“ bekommt man schließlich die StreamURLs und die Ziel-Mountpoints angezeigt.

.. image:: img/PD_Channel_StreamURL-fertig.png

.. seealso:: `Video-Tutorial "Einen Channel erstellen" <https://www.youtube.com/watch?v=YBApG9pms8c>`_ 





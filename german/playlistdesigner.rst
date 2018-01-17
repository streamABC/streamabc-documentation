.. index:: PlaylistDesigner

PlaylistDesigner
****************


.. index:: Werbeblöcke konfigurieren
.. index:: Werbeblöcke verteilen
.. index:: Automatische Werbeblöcke

Wenn ich 180 Sekunden über 3 Werbeblöcke verteile, wie ist dann der Algorithmus? 3 Blöcke á 60 Sekunden? Und wann spielt das System diese dann aus? Alle 20 Minuten? Und nach wie viel Minuten kommt der erste Werbeblock?
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Der Algorithmus ist sehr einfach. Wenn 180 Sekunden Werbezeit pro Stunde über 3 Werbeblöcke konfiguriert werden, 
dann werden in der Playlist automatisch 3 Werbeblöcke mit je 60 Sekunden eingefügt.

Das Intervall errechnet sich wie folgt:
60 Minuten / 3 Werbeböcke = 20 Minuten

Das Intervall beträgt 20 Minuten. Dass heißt, nach je 20 Minuten wird in diesem Beispiel ein Werbeblock automatisch in der Playlist eingefügt.

Aber der 1. Werbeblock wird bereits nach der Hälfte der Intervallzeit hinzugefügt.

Zusammengefasst:

- 1. Werbeblock mit 60 Sekunden nach 10 Minuten
- 2. Werbeblock mit 60 Sekunden nach 30 Minuten
- 3. Werbeblock mit 60 Sekunden nach 50 Minuten
- 3. Werbeblock mit 60 Sekunden nach 70 Minuten

usw.

Ergänzende Information zum Auslösen des Werbeblocks:

Der Werbeblock wird immer erst nach Ende des Audioelements eingefügt. 
Dass heißt, nach Ablauf der Intervallzeit spielt das Playout den aktuellen Audioinhalt noch zu Ende, und erst anschließend wird der Werbeblock aktiviert.
Mit Start des Werbeblocks wird auch das Intervall von 20 Minuten neu gestartet.




----

Bei weiteren Fragen bitte ein Ticket öffnen: |helpdesk|

Besuchen Sie unsere Unternehmens-Website |www.streamabc.com|



.. |helpdesk| raw:: html

    <a href="https://streamabc.zammad.com" target="_blank">https://streamabc.zammad.com</a>


.. |www.streamabc.com| raw:: html

   <a href="https://www.streamabc.com/#quantum-cast" target="_blank">www.streamabc.com/#quantum-cast</a>
   

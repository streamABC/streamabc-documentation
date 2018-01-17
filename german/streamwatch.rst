Streamwatch
***********



Gibt es ein Problem, wenn die aktuellen Hörersessions der letzten Stunden eingebrochen sind?
--------------------------------------------------------------------------------------------

.. image:: img/20180117_screenshot-streamwatch-listener-decrease-last-hours.png

Wenn nur die letzten Stunden der akt. Hörersessions einbrechen, 
aber sonst alles normal aussieht, 
dann gibt es kein Problem. Das ist normal.

Man muss dazu wissen, dass eine Hörersession erst dann gezählt und angezeigt wird, 
wenn der Hörer die Verbindung beendet hat. Die Daten der Hörersession werden dann der Stunde des Streamstarts zugezählt.

Ein Beispiel dazu:
    Ein Hörer schaltet morgens um 8:00 Uhr den Stream ein, und nachmittags um 14:00 Uhr wieder ab.
    Erst nach Ende das Streams, also nach 14:00 Uhr werden die Daten zu dieser Hörersession verarbeitet, und die Kurve wächst etwas an.
    Ich kann also die Daten des Hörers nicht schon um 12:00 Uhr sehen. 
    
Somit ist es normal, dass umso näher man der aktuellen Zeit in der Grafik kommt, desto mehr geht die Kurve nach unten.
**Die Hörerkurve wächst mit der Zeit nach oben.**
Im Extremfall kann es Hörersessions geben, welche mehrere Tage lang andauern. 
Dann kann auch die Anzahl der Hörersessions von vor Tage noch leicht anwachsen.


----

Wie ist es möglich, dass es mehr „max. parallele Hörer“ in einer Stunde gibt als Hörersessions?
-----------------------------------------------------------------------------------------------
.. image:: img/20180117_screenshot-streamwatch-max-listeners-compare-sessions.png

Jede Hörersession wird nur einmal gezählt und der Stunde des Streamstarts zugewiesen. 
Die Daten für parallele Hörer werden anders ermittelt und gezählt. 
Um die Anzahl der max. parallelen Hörer zu bekommen schaut ein Sensor permanent auf die Anzahl der gerade verbundenen Hörer.
Der Maximalwert der Stunde wird in der roten Linie angezeigt.

Ein Beispiel aus der Grafik:
    Alle Hörer, die zwischen 6:00 und 7:00 Uhr den Stream einschalten, 
    werden in grünen Linie am höchsten Punkt angezeigt. 
    Viele Hörer hörten den Stream nur kurz und zu unterschiedlichen Zeiten in der 6-7-Uhr-Stunde. 
    Dadurch gab es überdurchschnittlich viele Hörersessions in der Stunde. 
    Die Anzahl der gleichzeitig verbundenen Hörer stieg erst nach und nach an, weil immer wieder Hörersession beendet worden.
    Und es ist nur der höchste Wert in der Kurve „max. parallele Hörer“ dokumentiert.
    In der 9-10-Uhr-Stunde verhält es sich umgekehrt.
    Viele Hörer hörten den Stream über mehrere Stunden, werden aber nur in der 9-10-Uhr-Stunde bei Hörersessions einmal gezählt.
    Der Sensor für die Ermittlung der parallelen Hörer registriert auch in den Folgestunden die Hörer mit Streamstart aus der 9-10-Uhr-Stunde, solange bis diese Hörer abschalten.
    Somit ist es normal, dass max. parallelen Hörer deutlich höher sind als die Hörerseesion der Stunde.
    

    
----

Was bedeutet "Ø Verweildauer pro Hörer"?
---------------------------------------------

.. image:: img/20180117_screenshot-streamwatch-hoererverweildauer-bedeutung.png

Die durchschnittliche Hördauer in Stunden für jeden Hörer, mit einer Hördauer von mindestens einer Minute, innerhalb des definierten Zeitraumes. 
Dieser Wert wird berechnet: Gesamthördauer geteilt durch die Anzahl der Hörersessions des definierten Zeitraumes.


Ein Beispiel aus der Grafik:
    Die Verweildauer wird in Stunden angegeben. In diesem Beispiel beträgt der Wert 1.844 in der 9:00 Uhr-Stunde.
    Das heißt, dass von 9:00 Uhr bis 10:00 Uhr ein Hörer im Durchschnitt eine Hördauer von 1,844 Stunden hatte.
    1,844 Stunden = 110 Minuten und 38 Sekunden.


----

Besuchen Sie unsere Unternehmens-Website |www.streamabc.com|

.. |www.streamabc.com| raw:: html

   <a href="https://www.streamabc.com/#quantum-cast" target="_blank">www.streamabc.com/#quantum-cast</a>
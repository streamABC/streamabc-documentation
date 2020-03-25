.. index:: Troubleshooting
.. index:: Fehlerbehebung

Troubleshooting
***************


.. index:: Werbung mitten im Stream

Werbung mitten im Stream, während der Musik oder während der Nachrichten
------------------------------------------------------------------------

Es gibt zwei mögliche Szenarien:

    1. Wenn alle Hörer das gleiche Problem haben
    #. Wenn es vereinzelte Hinweise von Hörern dazu gibt


Zu 1.)
    Wenn alle Hörer das gleiche Problem haben, dann wird die Instream-Werbung falsch getriggert.
    Um das Problem zu beheben, müssen die Werbeauslöser überprüft und angepasst werden. 
    Weitere Information dazu unter:
    `Wie wird In-Stream Audio Ad ausgelöst? <http://streamabc-documentation.readthedocs.io/de/latest/werbung.html#wie-wird-in-stream-audio-ad-ausgelost>`_

Zu 2.)
    Sollte es vereinzelte Hinweise von Hörern geben, oder das Problem scheinbar immer mal wiederauftauchen, aber nicht reproduzierbar sein, dann ist die Ursache ziemlich sicher ein Verbindungsproblem beim Hörer.
    Beim Verbindungsabbruch des Hörers wird der Stream sofort neu verbunden. Aber mit Neuverbindung wird dann ein Prerollspot ausgespielt. 
    Für den Hörer hört es sich dann so an, als ob eine Werbung mitten im Song läuft.
    Um das Problem zu beheben, muss entweder die Ursache des Verbindungsabbruchs gefunden und behoben werden.
    Oder der Player/die App sollte lernen, bei einer automatischen Neuverbindung den Prerollspot zu unterdrücken.
    Die Ursache für einzelne Verbindungsabbrüche zu finden, ist meist nicht einfach und häufig gar nicht möglich.
    Am Einfachsten ist es den Prerollspot durch die App zu unterdrücken, wenn der Stream ungeplant verloren geht. 


    








----

Bei weiteren Fragen bitte ein Ticket öffnen: |helpdesk|

Besuchen Sie unsere Unternehmens-Website |www.quantumcast-digital.de|



.. |helpdesk| raw:: html

    <a href="https://streamabc.zammad.com" target="_blank">https://streamabc.zammad.com</a>


.. |www.quantumcast-digital.de| raw:: html

   <a href="https://www.quantumcast-digital.de" target="_blank">www.quantumcast-digital.de</a>

.. |Console| raw:: html

   <a href="https://www.quantumcast-digital.de" target="_blank">Console</a>
   

# Aufgabenblatt 24

ifconfig eth0 down
modprobe -r pcnet32
---

**Aufgabe 1**

Was haben Sie soeben durchgeführt?

`Netzwerk Adapter und Treiber dekativiert.`

**Aufgabe 2**

Was zeigt das Kommando **ifconfig** und **route** Ihnen nun bzgl. eht0 an?

`Keine Informationen mehr dazu.`


**Aufgabe 3**

Wie können Sie dies wieder beheben?

`sudo ifconfig eth0 up modprobe pcnet32`


**Aufgabe 4**

Aktivieren Sie die Netzwerkkarte wieder. Wie sieht die Routingtabelle aus?

`Es sieht so aus wie ganz am Anfang bevor wir es deaktiviert haben.`


**Aufgabe 5**

Machen Sie die Netzwerkverbindung wieder gangbar.

`sudo ifconfig eth0 up modprobe pcnet32`


**Aufgabe 6**

Überprüfen Sie die Funktion der Karte, indem Sie Google anpingen. Wie sieht ihre Routingtabelle nun aus? Was schließen Sie allgemein daraus?

`Routingtabelle sieht unverändert aus bis auf, dass die Anzahl bei Use höher gezählt ist.`

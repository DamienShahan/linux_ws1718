# Aufgabenblatt 13

**Aufgabe 1**

Schreiben Sie ein Skript namens "welcome.sh", das Sie mit Ihrem Namen Begrüßt und Ihnen die aktuelle Uhrzeit in ihrem bevorzugten Format angibt.

`touch welcome.sh`

`#!/bin/bash`

`echo "Hallo $USER, es ist $(date +%T)"`

**Aufgabe 2**

Modifizieren Sie das Skript derart, dass Sie und die Mitglieder Ihrer Gruppe es ausführen können.

`chmod 774 welcome.sh`


**Aufgabe 3**

Erweitern Sie das Skript nun derart, dass es Ihnen zusätzlich eine lexikografisch absteigend sortierte Liste der Pfade in ihrem Home-Verzeichnis ausgibt.

`find $HOME -maxdepth 1 ! -name '.*' | sort -r`


**Aufgabe 4**

Erweitern Sie das Skript nun so, dass die Pfade aus 3. in einer Variable gespeichert werden. Wie schaffen Sie es, dass jeder Pfad in einer eigenen Zeile steht?

`pfadVar=$(find $HOME -maxdepth 1 ! -name '.*' | sort -r)`

`echo -e "$pfadVar"`

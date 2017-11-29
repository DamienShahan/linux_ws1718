# Aufgabenblatt 21

**Aufgabe 1**

Erstellen Sie ein Skript, welches die aktuelle Speicherplatzbelegung des Homelaufwerks, des Benutzers in eine Datei in dessen Homelaufwerk speichert. Fehlermeldungen sollen zu /dev/null weitergeleitet werden.
- Das Skript sollte über einen Start, Stop und Restart Bereich verfügen.
- Bei Start soll getestet werden ob die Datei erstellt werden kann und anschließend erstellt werden
- Bei Stop soll getestet werden ob eine Datei vorhanden ist und diese gelöscht werden
- Bei Restart soll falls vorhanden die Datei gelöscht und neu erstellt werden.

`~/Playground/Sandbox/discusage.sh`

**Aufgabe 2**

Erstellen Sie ein Startskript, welches bei den Runleveln 2-5 das eben erstellte Skript ausführt, bei allen anderen soll dieses gestoppt werden.

`/etc/init.d/discusageRunlevel.sh`


**Aufgabe 3**

Aktuallisieren Sie die Runlevel mittels **update-rc.d**

`update-rc.d discusageRunlevel.sh defaults`

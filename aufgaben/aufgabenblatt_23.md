# Aufgabenblatt 23

Erstellen Sie ein Backup-Skript, das das Home-Verzeichnis des übergebenen Benutzernamens sichert. Dokumentieren Sie ihr Vorgehen ausführlich.
---

**Aufgabe 1**

Auf welche Partition sollte die Sicherung stattfinden?

`Backup Partition`

**Aufgabe 2**

Erzeugen Sie dort ein Backup-Verzeichnis, sofern dies nicht schon existiert.

`mkdir 755 /backup/`


**Aufgabe 3**

Erzeugen Sie dort ein Unterverzeichnis mit dem Usernamen, sofern dies nicht schon existiert.

`mkdir 755 /backup/shahand/`


**Aufgabe 4**

Der Archivname soll Datum und Uhrzeit enthalten (dd-mm-yy-hh-mm).

`tar cfv "/backup/shahand/archiv..$(date +%Y-%m-%d-%H-%M).tar" ~/`


**Aufgabe 5**

Löschen Sie zuvor ein vorhandenes Backup dieses Users, sofern dies älter als fünf Minuten ist.

`touch ~/Playground/Sandbox/backupScript.sh`
`find /backup/shahand/* -mmin +5 -exec rm {} \;`


**Aufgabe 6**

Richten Sie einen Cron-Job für Ihr Backup-Skript ein, der jeden Freitag um 23:00 Uhr ausgeführt wird.

`crontab -e`
`0 23 * * FRI ~/Playground/Sandbox/backupScript.sh`

# Aufgabenblatt 19

**Aufgabe 1**

Korrigieren Sie die Ausgabe des letzten Kommandos auf der vorherigen Seite dahingehend das die Ausgabe „1 Schaf springt über den Zaun" berücksichtigt.

`echo "1 Schaf springt über den Zaun" && seq -f "%1g Schafe springen über den Zaun" 2 100`

**Aufgabe 2**

Verwenden Sie die arithmetische Substitution um herauszufinden, welche Zahlen von 456 bis 675 restlos durch 16 Teilbar sind. Geben Sie nur die restlos teilbaren Zahlen aus. Sollte der Modulo-Wert kleiner als 5 sein, leiten Sie das Ergebnis an Stderr weiter. Sollte er größer sein, an das Null-Device.

`Zu finden unter: ~/Playground/Sandbox/restlosTeilbar.sh`

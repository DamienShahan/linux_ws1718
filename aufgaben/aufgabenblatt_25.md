# Aufgabenblatt 25

**Aufgabe 1**

Machen Sie einen ping auf den Host mbc.fh-trier.de . Wie ist seine IP-Adresse?

`143.93.51.132`

**Aufgabe 2**

Prüfen Sie nun die IP-Adresse des Hosts mbc.fh-trier.de über nslookup. Welches Resultat erhalten Sie?

`Die gleiche IP-Adresse. Meine etc/hosts Datei ist nicht manipultiert.`


**Aufgabe 3**

Wie ist der Hostname ihres Systems?

`hostname linux-fh-trier`


**Aufgabe 4**

Machen Sie einen ping auf Ihren Hostname. Wie ist seine IP-Adresse?

`127.0.1.1`


**Aufgabe 5**

Prüfen Sie nun die IP-Adresse Ihres Hosts über nslookup. Welches Resultat erhalten Sie?

`reverse lookup 1.1.0.127.in-addr.arpa`


**Aufgabe 6**

Was folgern Sie aus den beiden Resultaten?

`Ping durchläuft zuerst die etc/hosts und dann zum DNS Server, wobei ein nslookup direkt zum DNS Server routet.`

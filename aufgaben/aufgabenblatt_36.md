#Aufgabenblatt 36
 
Gehen Sie davon aus, das Ihr Server mittels IP-Tables gesichert ist.

**Aufgabe 1**

Sichern Sie die bestehende Firewall-Konfiguration an einem geeigneten Ort mit dem aktuellen Zeitstempel.

`iptables-save > /var/backup/iptables.${date+"%s"}.txt`

**Aufgabe 2**

Leeren Sie die Konfiguration von iptables.

`iptables -L`

**Aufgabe 3**

Erstellen Sie eine Firewall-Regel, welche den Internetverkehr über das HTTP-Protokoll zum Server ermöglicht, achten sie dabei auf die Default-Policies.

`iptables -A INPUT -p tcp -m tcp --dport 80 -j ACCEPT`

**Aufgabe 4**

Erstellen Sie eine Firewall-Regel, welche den Internetverkehr über das HTTPS-Protokoll zum Server ermöglicht, achten sie dabei auf die Default-Policies.

`iptables -A INPUT -p tcp -m tcp --dport 443 -j ACCEPT`

**Aufgabe 5**

Erstellen Sie eine Firewall-Regel, welche die DNS-Namensauflösung ermöglicht (Client), achten sie dabei auf die Default-Policies.

`# UDP`
`iptables -A INPUT -i eth0 -p udp --sport 53 -j ACCEPT`
`iptables -A OUTPUT -o eth0 -p udp --dport 53 -j ACCEPT`
`# TCP`
`iptables -A INPUT -i eth0 -p tcp --sport 53 -j ACCEPT`
`iptables -A OUTPUT -o eth0 -p tcp --dport 53 -j ACCEPT`

**Aufgabe 6**

Ein Ping auf das System darf aus Sicherheitsgründen **nicht** möglich sein, achten sie dabei auf die Default-Policies.

`iptables -A INPUT -p icmp --icmp-type 8 -j DROP`

**Aufgabe 7**

Laden Sie die gesicherte Konfiguration aus der Datei zurück in die Firewall.

`iptables-restore < /var/backup/iptables*`

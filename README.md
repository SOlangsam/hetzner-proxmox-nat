# hetzner-proxmox-nat
Kleines Rep zur Konfiguration von Proxmox in Verbindung mit NAT. 

Hier beschreibe ich die Möglichkeit mehrere VMs mit nur einer Public IP zu nutzen.
Dazu nutzen wir den Host als Router und erlauben das IP-Forwarding.

Wichtig ist, dass für jede IP bzw. jeden Port, der nach außen erreichbar sein soll, eine Freigabe in der /etc/network/interfaces erfolgen muss!

Bei jeder Änderung muss am besten ein Reboot von allen Systemen durchgeführt werden!


*Update*
Heute möchte ich mein Repo um die Möglichkeit ergänzen, statt die Ports für jedgliche Anwendung freizuschalten, einen VPN Zugang zu nutzen.
Vorteil liegt ganz klar auf der Hand. Host System lauscht nicht auf allen möglichen Ports nach außen, es hält nur den VPN Port offen

Hauptgrund für mich ist die Möglichkeit mehrere RDP Verbindungen mit den gleichen Ports auf einer IP zu nutzen.
Natürlich kann man das auch alles mit einem Reverse Proxy mit Subdomains steuern oder man nutzt weitere IPs.

Derzeit nutze ich OpenVPN, überlege aber zu Wireguard zu wechseln.
VPN gewinnt dadurch enorm an Performance.
Da es aber für die täglichen Arbeiten ausreicht und Wireguard kein UDP unterstützt, bleibe ich vorerst bei OpenVPN

Datei zur Konfiguration folgt...

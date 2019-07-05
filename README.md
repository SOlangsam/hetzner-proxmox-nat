# hetzner-proxmox-nat
Kleines Rep zur Konfiguration von Proxmox in Verbindung mit NAT. 

Hier beschreibe ich die Möglichkeit mehrere VMs mit nur einer Public IP zu nutzen.
Dazu nutzen wir den Host als Router und erlauben das IP-Forwarding.

Wichtig ist, dass für jede IP bzw. jeden Port, der nach außen erreichbar sein soll, eine Freigabe in der /etc/network/interfaces erfolgen muss!

Bei jeder Änderung muss am besten ein Reboot von allen Systemen durchgeführt werden!

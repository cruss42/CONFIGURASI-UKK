# CONFIGURASI-WINBOX

IP ADDRESS
172.16.100.36/24 = ETHER 1
192.168.36.1/29 = ETHER 3
192.168.100.1/24 = ETHER 2

FIREWALL
Chain = scrnat
Out Interface to ether 1
Chain = dstnat
Action = masquerade
Dst. Address = 172.16.100.36
Dst. Port = 9090
Action = dst-nat
To Address = 192.168.36.2
To Port = 80

DNS = 8.8.8.8 - 1.1.1.1
DHCP SERVER to ether 2

Routes
Gateway = 172.16.100.254

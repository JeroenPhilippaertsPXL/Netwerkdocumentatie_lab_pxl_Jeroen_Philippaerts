# Netwerkdocumentatie_lab_pxl_Jeroen_Philippaerts
LAB opdracht pxl

Netwerk configuratie voor R1 
service password-encryption
security passwords min-length 5


hostname R1
/n
enable secret 5 class
!
username jeroen secret 5 cisco
!
ip domain-name cisco.com
!
interface GigabitEthernet0/0/0
description "connection to SW1"
ip address 192.168.0.2 255.255.255.240
duplex auto
speed auto
ipv6 address 2001:DB8:ACAD::1/64
no shutdown
!
interface GigabitEthernet0/0/1
ip address 192.168.0.17 255.255.255.240
duplex auto
speed auto
no shutdown
!
interface Vlan1
no ip address
shutdown
!
ip default-gateway 192.168.0.1
!
banner motd ^CWarning: Unauthorized acces is prhobited!^C
!
line con 0
password 7 cisco
login
!
line aux 0
!
line vty 0 4
password 7 cisco
login
transport input ssh
line vty 5 15
password 7 cisco

Netwerk configuratie voor SW1 en SW2

# Netwerkdocumentatie_lab_pxl_Jeroen_Philippaerts
LAB opdracht pxl



<pre>
Configuratie R1
  
service password-encryption
security passwords min-length 5
!
hostname R1
!
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
!
interface GigabitEthernet0/0/1
ip address 192.168.0.17 255.255.255.240
duplex auto
speed auto
ipv6 address 2001:db8:acad:1::1/64
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

  Configuratie SW1 en SW2

service password-encryption
!
hostname SW1
!
enable secret 5 class
!
ip domain-name cisco.com
!
username bob secret 5 cisco
!
interface FastEthernet0/1
!
interface FastEthernet0/2
!
interface FastEthernet0/3
!
interface FastEthernet0/4
!
interface FastEthernet0/5
!
interface FastEthernet0/6
!
interface FastEthernet0/7
!
interface FastEthernet0/8
!
interface FastEthernet0/9
!
interface FastEthernet0/10
!
interface FastEthernet0/11
!
interface FastEthernet0/12
!
interface FastEthernet0/13
!
interface FastEthernet0/14
!
interface FastEthernet0/15
!
interface FastEthernet0/16
!
interface FastEthernet0/17
!
interface FastEthernet0/18
!
interface FastEthernet0/19
!
interface FastEthernet0/20
!
interface FastEthernet0/21
!
interface FastEthernet0/22
!
interface FastEthernet0/23
!
interface FastEthernet0/24
!
interface GigabitEthernet0/1
!
interface GigabitEthernet0/2
!
interface Vlan1
 description "connection to R1"
 ip address 192.168.0.13 255.255.255.240
!
ip default-gateway 192.168.0.1
!
banner motd ^CWarning:Unauthorized acces is prohibited!^C
!
!
!
line con 0
 password 7 0822455D0A16
 login
!
line vty 0 4
 exec-timeout 5 30
 password 7 0822455D0A16
 login
 transport input ssh
line vty 5 15
 exec-timeout 5 30
 password 7 0822455D0A16
 login
 transport input ssh
</pre>


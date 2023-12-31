# Jarkom-Modul-4-D04-2023
# Anggota Kelompok
|                Nama                |    NRP     |
| :--------------------------------: | :--------: |
|            Daffa Saskara           | 5025211249 |
|      Arundaya Pratama Nurhasan     | 5025221206 |
## Soal
1. Soal shift dikerjakan pada Cisco Packet Tracer dan GNS3 menggunakan metode perhitungan CLASSLESS yang berbeda.
Keterangan: Bila di CPT menggunakan VLSM, maka di GNS3 menggunakan CIDR atau sebaliknya
2. Jika tidak ada pemberitahuan revisi soal dari asisten, berarti semua soal BERSIFAT BENAR dan DAPAT DIKERJAKAN.
3. Untuk di GNS3 CLOUD merupakan NAT1 jangan sampai salah agar bisa terkoneksi internet.
4. Pembagian IP menggunakan Prefix IP yang telah ditentukan pada modul pengenalan
5. Pembagian IP dan routing harus SE-EFISIEN MUNGKIN.
# Topologi dan Pembagian Subnet
## Cisco Packet Tracer
![cidrcpt](https://github.com/Sirund/Jarkom-Modul-4-D24-2023/assets/88588446/6aa1226a-94d4-448a-861c-09abab8a2252)
### CPT Tree
![cidrtree](https://github.com/Sirund/Jarkom-Modul-4-D24-2023/assets/88588446/9084e75f-eebf-401b-b038-6f51fbe7ae6b)
### CPT Pembagian IP
![cptip](https://github.com/Sirund/Jarkom-Modul-4-D24-2023/assets/88588446/1f77bdec-3e47-464b-9abc-75f8784d9aa4)
## GNS3
![Topologi_gns](https://github.com/Sirund/Jarkom-Modul-4-D24-2023/assets/120204570/874b1906-d0f9-41f3-b287-a3b3067a7f26)
## VLSM
### VLSM Tree
![Diagram Tanpa Judul drawio (1)](https://github.com/Sirund/Jarkom-Modul-4-D24-2023/assets/120204570/de33ee17-5957-4662-b36e-6be845befd33)
### Pembagian IP
![Screenshot from 2023-12-06 19-10-58](https://github.com/Sirund/Jarkom-Modul-4-D24-2023/assets/120204570/8787ac8d-9c6f-4758-876a-9d3e82edc493)
### Konfigurasi dan Routing
Dibawah ini adalah konfigurasi jaringan tiap node pada topologi diatas
- Aura (Main Router)
```bash
auto eth0
iface eth0 inet dhcp

#16
auto eth1
iface eth1 inet static
	address 192.203.24.141
	netmask 255.255.255.252

#17
auto eth2
iface eth2 inet static
	address 192.203.24.145
	netmask 255.255.255.252

#12
auto eth3
iface eth3 inet static
	address 192.203.24.129
	netmask 255.255.255.252
```
- Denken (Router)
```bash
#18
auto eth0
iface eth0 inet static
	address 192.203.23.1
	netmask 255.255.255.0

#17
auto eth2
iface eth2 inet static
	address 192.203.24.146
	netmask 255.255.255.252
```
- Frieren (Router)
```bash
#15
auto eth0
iface eth0 inet static
	address 192.203.24.137
	netmask 255.255.255.252

#16
auto eth1
iface eth1 inet static
	address 192.203.24.142
	netmask 255.255.255.252

#20
auto eth2
iface eth2 inet static
	address 192.203.24.65
	netmask 255.255.255.224
```
- Flamme (Router)
```bash
#15
auto eth0
iface eth0 inet static
	address 192.203.24.138
	netmask 255.255.255.252

#14
auto eth1
iface eth1 inet static
	address 192.203.12.1
	netmask 255.255.252.0

#19
auto eth2
iface eth2 inet static
	address 192.203.24.149
	netmask 255.255.255.252

#11
auto eth3
iface eth3 inet static
	address 192.203.24.125
	netmask 255.255.255.252
```
- Fern (Router)
```bash
#21
auto eth0
iface eth0 inet static
	address 192.203.0.1
	netmask 255.255.248.0

#19
auto eth2
iface eth2 inet static
	address 192.203.24.150
	netmask 255.255.255.252
```
- Himmel (Router)
```bash
#6
auto eth0
iface eth0 inet static
	address 192.203.24.97
	netmask 255.255.255.248

#11
auto eth3
iface eth3 inet static	
	address 192.203.24.126
	netmask 255.255.255.252
```
- Eisen (Router)
```bash
#8
auto eth0
iface eth0 inet static
	address 192.203.24.105
	netmask 255.255.255.248

#13
auto eth1
iface eth1 inet static
	address 192.203.24.133
	netmask 255.255.255.252

#9
auto eth2
iface eth2 inet static
	address 192.203.24.121
	netmask 255.255.255.252

#12
auto eth3
iface eth3 inet static
	address 192.203.24.130
	netmask 255.255.255.252

#7
auto eth4
iface eth4 inet static
	address 192.203.24.117
	netmask 255.255.255.252
```
- Lugner (Router)
```bash
#10
auto eth0
iface eth0 inet static
	address 192.203.8.1
	netmask 255.255.252.0

#5
auto eth1
iface eth1 inet static
	address 192.203.22.1
	netmask 255.255.255.0

#9
auto eth2
iface eth2 inet static
	address 192.203.24.122
	netmask 255.255.255.252
```
- Linie (Router)
```bash
#4
auto eth0
iface eth0 inet static
	address 192.203.24.113
	netmask 255.255.255.252

#2
auto eth1
iface eth1 inet static
	address 192.203.20.1
	netmask 255.255.254.0

#7
auto eth4
iface eth4 inet static
	address 192.203.24.118
	netmask 255.255.255.252
```
- Lawine (Router)
```bash
#4
auto eth0
iface eth0 inet static
	address 192.203.24.113
	netmask 255.255.255.252

#2
auto eth1
iface eth1 inet static
	address 192.203.20.1
	netmask 255.255.254.0

#7
auto eth4
iface eth4 inet static
	address 192.203.24.118
	netmask 255.255.255.252
```
- Heiter (Router)
```bash
#1
auto eth0
iface eth0 inet static
	address 192.203.16.1
	netmask 255.255.252.0

#3
auto eth2
iface eth2 inet static
	address 192.203.24.2
	netmask 255.255.255.192
```
- Stark (Server)
```bash
#13
auto eth0
iface eth0 inet static
	address 192.203.24.134
	netmask 255.255.255.252
	gateway 192.203.24.133
```
- Richter (Server)
```bash
#8
auto eth1
iface eth1 inet static
	address 192.203.24.106
	netmask 255.255.255.248
	gateway 192.203.24.105
```
- Revolte (Server)
```bash
#8
auto eth2
iface eth2 inet static
	address 192.203.24.107
	netmask 255.255.255.248
	gateway 192.203.24.105
```
- Sein (Server)
```bash
#1
auto eth2
iface eth2 inet static
	address 192.203.16.3
	netmask 255.255.252.0
	gateway 192.203.16.1
```
- LaubHills (397 host)
```bash
#21 
auto eth2
iface eth2 inet static
	address 192.203.0.3
	netmask 255.255.248.0
	gateway 192.203.0.1
```
- AppetitRegion (625 host)
```bash
#21 
auto eth1
iface eth1 inet static
	address 192.203.0.2
	netmask 255.255.248.0
	gateway 192.203.0.1
```
- LakeKorridor (24 host)
```bash
#14 
auto eth0
iface eth0 inet static
	address 192.203.24.66
	netmask 255.255.255.224
	gateway 192.203.24.65
```
- RohrRoad (1000 host)
```bash
#14 
auto eth0
iface eth0 inet static
	address 192.203.12.2
	netmask 255.255.252.0
	gateway 192.203.12.1
```
- RoyalCapital (63 host)
```bash
#18
auto eth1
iface eth1 inet static
	address 192.203.23.2
	netmask 255.255.255.0
	gateway 192.203.23.1
```
- WilleRegion (63 host)
```bash
#18
auto eth2
iface eth2 inet static
	address 192.203.23.3
	netmask 255.255.255.0
	gateway 192.203.23.1
```
- TurkRegion (1000 host)
```bash
#10
auto eth1
iface eth1 inet static
	address 192.203.8.2
	netmask 255.255.252.0
	gateway 192.203.8.1
```
- GrobeForest (250 host)
```bash
#5
auto eth0
iface eth0 inet static
	address 192.203.22.2
	netmask 255.255.255.0
	gateway 192.203.22.1
```
- GranzChannel (254 host)
```bash
#2
auto eth0
iface eth0 inet static
	address 192.203.20.2
	netmask 255.255.254.0
	gateway 192.203.20.1
```
- BredtRegion (29 host)
```bash
#3
auto eth0
iface eth0 inet static
	address 192.203.24.3
	netmask 255.255.255.192
	gateway 192.203.24.1
```
- RiegelCanyon (510 host)
```bash
#1
auto eth1
iface eth1 inet static
	address 192.203.16.2
	netmask 255.255.252.0
	gateway 192.203.16.1
```
- SchwerMountains (5 host)
```bash
#6
auto eth1
iface eth1 inet static
	address 192.203.24.98
	netmask 255.255.255.248
	gateway 192.203.24.97
```
Kemmudian konfigurasi routing pada tiap node dengan melakukan command berikut
- Aura
```bash
route add -net 192.203.23.0 netmask 255.255.255.0 gw 192.203.24.146 #18

route add -net 192.203.24.64 netmask 255.255.255.224 gw 192.203.24.142 #20
route add -net 192.203.12.0 netmask 255.255.252.0 gw 192.203.24.142 #14
route add -net 192.203.24.136 netmask 255.255.255.252 gw 192.203.24.142 #15
route add -net 192.203.24.96 netmask 255.255.255.248 gw 192.203.24.142 #6
route add -net 192.203.24.96 netmask 255.255.255.248 gw 192.203.24.142 #11
route add -net 192.203.24.96 netmask 255.255.255.248 gw 192.203.24.142 #19
route add -net 192.203.0.0 netmask 255.255.248.0 gw 192.203.24.142 #21

route add -net 192.203.22.0 netmask 255.255.255.0 gw 192.203.24.130 #5
route add -net 192.203.8.0 netmask 255.255.252.0 gw 192.203.24.130 #10
route add -net 192.203.20.0 netmask 255.255.254.0 gw 192.203.24.130 #2
route add -net 192.203.24.132 netmask 255.255.255.252 gw 192.203.24.130 #13
route add -net 192.203.24.104 netmask 255.255.255.248 gw 192.203.24.130 #8
route add -net 192.203.24.120 netmask 255.255.255.252 gw 192.203.24.130 #9
route add -net 192.203.24.116 netmask 255.255.255.252 gw 192.203.24.130 #7
route add -net 192.203.24.0 netmask 255.255.255.192 gw 192.203.24.130 #3
route add -net 192.203.24.112 netmask 255.255.255.252 gw 192.203.24.130 #4
route add -net 192.203.16.0 netmask 255.255.252.0 gw 192.203.24.130 #1
```
- Denken
```bash
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.203.24.145 #17
```
- Frieren
```bash
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.203.24.141 #16 

route add -net 192.203.12.0 netmask 255.255.252.0 gw 192.203.24.138 #14
route add -net 192.203.24.96 netmask 255.255.255.248 gw 192.203.24.138 #6
route add -net 192.203.0.0 netmask 255.255.248.0 gw 192.203.24.138 #21 
route add -net 192.203.24.148 netmask 255.255.255.252 gw 192.203.24.138 #19
route add -net 192.203.24.124 netmask 255.255.255.252 gw 192.203.24.138 #11
```
- Flamme
```bash
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.203.24.137 #15

route add -net 192.203.0.0 netmask 255.255.248.0 gw 192.203.24.150 #21 
route add -net 192.203.24.96 netmask 255.255.255.248 gw 192.203.24.126 #6
```
- Fern
```bash
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.203.24.149 #19
```
- Himmel
```bash
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.203.24.125 #11
```
- Eisen
```bash
#8
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.203.24.129 #12

route add -net 192.203.22.0 netmask 255.255.255.0 gw 192.203.24.122 #5
route add -net 192.203.8.0 netmask 255.255.252.0 gw 192.203.24.122 #10

route add -net 192.203.20.0 netmask 255.255.254.0 gw 192.203.24.118 #2
route add -net 192.203.24.0 netmask 255.255.255.192 gw 192.203.24.118 #3
route add -net 192.203.24.112 netmask 255.255.255.252 gw 192.203.24.118 #4
route add -net 192.203.16.0 netmask 255.255.252.0 gw 192.203.24.118 #1
```
- Lugner
```bash
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.203.24.121
```
- Linie
```bash
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.203.24.117 #7

route add -net 192.203.24.0 netmask 255.255.255.192 gw 192.203.24.114 #3
route add -net 192.203.16.0 netmask 255.255.252.0 gw 192.203.24.114 #1
```
- Lawine
```bash
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.203.24.113 #4

route add -net 192.203.16.0 netmask 255.255.252.0 gw 192.203.24.2 #1
```
- Heiter
```bash
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.203.24.1 #3
```

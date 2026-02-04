Switch Config
1. Setting switch dan PC seperti vlan biasa.
	#vlan10
	#name nama_vlan10
2. Pilih int range.
	#int range fa0/1 - 8
	#switchport mode access
	#switchport access vlan 10
	#show vlan brief ---> Untuk mengecek interfaces
3. Hubungkan switch dengan router pada port gigabit.
4. Atur port switch yang digunakan menjadi mode trunk.
	#switchport mode trunk
	#show interfaces trunk

Router Config
1. Nyalakan port yang digunakan. 
	#int gig0/0
	#no sh
2. Buat sub-interfaces VLAN 10 20 dan 30
	#int gig0/0.10
	#encapsulation dot1Q 10
	#ip address 192.168.10.1 255.255.255.0
3. Untuk VLAN 20 dan 30 lakukan cara yang sama.
4. Kecualikan Ip router VLAN 10 20 dan 30
	#ip dhcp excluded-address 192.168.10.1
	#ip dhcp excluded-address 192.168.20.1
	#ip dhcp excluded-address 192.168.30.1
5. Bikin DHCP pool untuk masing masing VLAN.
	#ip dhcp pool nama_VLAN
	#network NA_VLAN
	#default-router ip_VLAN
	#dns-server  8.8.8.8

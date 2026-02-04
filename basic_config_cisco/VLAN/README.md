A. VLAN dengan 1 Switch
1. Masuk ke cli switch.
2. (optional) Beri nama VLAN.
	#vlan 10
	#name nama_vlan
3. Pilih interface, ubah mode port, dan access vlan.
	#int range fa0/1 - 10
	#switchport mode access
	#switchport access vlan 10
4. Lakukan pengecekan table.
	#show vlan brief

B. VLAN dengan multi switch
1. Setting VLAN pada masing-masing switch dengan cara biasa.
2. Sisakan satu/beberapa port untuk ke switch lainnya. (fa0/24 digunakan sbg trunk)
3. Hubungkan kedua switch dengan port yang dipilih.
4. Atur port menjadi mode trunk pada masing-masing switch
	#int fa_yang dipilih
	#switchport mode trunk

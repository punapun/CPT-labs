1. Berikan router IP Address terlebih dahulu.
2. Kecualikan ip router (mode privilege),	# ip dhcp excluded-address ip_router
3. Masuk ke mode DHCP, 	#ip dhcp pool nama_dhcp
4. Masukkan NA,		#network NA
5. Atur gateway, 	#default-router ip_router
6. Atur dns, 		#dns-server 8.8.8.8

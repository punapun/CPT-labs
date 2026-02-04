Konfigurasi router cisco dengan simulasi pada Cisco Packet Tracer

A. Dasar Router Cisco
• IOS – Internetwork Operating System
• 3 sistem utama/mode Cisco IOS --> 1. User exec 				Router>
						            2. Privilege exec, enable		Router#
						            3. Global configuration, conf t	Router(config)#
• Mengubah hostname, di mode Global config,	#hostname nama_router
• Cara setting password, di mode Global config
	1. Password user exec,	#enable password 12345
	2. Password privilage exec,	#line console 0 (masuk ke line console)
					#password 1234 (berikan pass)
					#login (aktifkan pass)
• Password tersimpan pada format plain text, di mode privilage	#show running-config
• Cara men-enkripsi password, di mode Global config, 	#enable secret belajar
• Cara set MOTD, Global config 	#banner motd &Isi_pesan&
• Dua jenis config pada cisco router
	1. #show running-config
	2. #show startup-config, menyimpan running configuration :
	mode privilage: #copyrunning-config startup-config

B. Konfigurasi Router Cisco
• Masuk ke Global config
• Pilih interface,			    #interface nama_interface
• Beri Ip Address sesuai NA, 	#ip address 192.168.1.254 255.255.255.0
• Berikan default gateway dengan ip adress router, agar router dapat menjembatani NA yang berbeda.

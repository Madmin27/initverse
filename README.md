# initverse
initverse node service komutu


Servis dosyası olarak kullanmak isterseniz

	  nano /etc/systemd/system/iniminer.service içersine atabilirsiniz
*** xxx leri cüzdan adresiniz ve node isminizle değiştitirin

		[Unit]
		Description=Iniminer Node Service
		After=network-online.target
		
		[Service]
		ExecStart=/root/./iniminer-linux-x64 --pool stratum+tcp://0xF6D39Dda8997407110264acEc6axxxx639.isimxxx@pool-core-testnet.inichain.com:32672 --cpu-devices 1 --cpu-devices 2 --cpu-devices 3 --cpu-devices 4 --cpu-devices 5 --cpu-devices 6 --cpu-devices 7 --cpu-devices 8 --cpu-devices 9 --cpu-devices 10 --cpu-devices 11
		Restart=always
		User=root
		Group=root
		
		[Install]
		WantedBy=multi-user.target




 Çalıştırmak için de 
 
    systemctl daemon-reload &&  systemctl enable iniminer &&  systemctl start iniminer

    journalctl -u iniminer -f -o cat

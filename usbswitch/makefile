

install:
	cp 40_DWA-171.rules /etc/udev/rules.d/
	cp "0bda:1a2b" /etc/usb_modeswitch.d/
	echo "2001:331d" | sudo tee --append /var/lib/usb_modeswitch/bind_list
	service udev restart

uninstall:
	rm /etc/udev/rules.d/40_DWA-171.rules
	rm "/etc/usb_modeswitch.d/0bda:1a2b"
	sed -e "s/2001:331d//g" -i /var/lib/usb_modeswitch/bind_list
	service udev restart
		
all: install



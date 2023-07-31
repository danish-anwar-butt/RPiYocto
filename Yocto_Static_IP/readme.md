# How to set static IP in Yocto running on Raspberry Pi 3

1. Edit **/etc/network/interface** file and add following lines for Ethernet

   

   `auto eth0
   iface eth0 inet static
   	address 192.168.1.2
   	netmask 255.255.255.0`

   

2. Go to **cd /var/lib/connman/** and create file **ethernet_eth0.config** with following content:

   `[service_ethernet_eth0]
   Type=ethernet
   IPv4=192.168.1.2/24
   IPv4Gateway=192.168.1.1
   IPv4ConfigurationMethod=manual`

3.  Restart the networkmanager using:

   `/etc/init.d/networking restart`

4. check the IP address using following command

   `ip addr show eth0`

5. Reboot the RPi using `reboot` command
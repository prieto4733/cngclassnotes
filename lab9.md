# Lab 9

---

4b. The command that I used to create example1 connection: 
    nmcli con add con-name (name) type (type) ifname (interface) ip.address (ip) ip.gateway (gateway)

9. I think mainly why example1 network was that the ip address was different from the normal ethernet connection that I had.

12. The system hostname is located in /etc/hosts

13. The value of /etc/hosts is very important because this file is where the hostname is stored. It will be able to be reached from the 
    outside because of this file.

14. RHEL determines the name of the interface by the firmware of the device. if its on board or on the pci bus and sockets, they get the 
    name depending of these variables.

15. the name of my NIC is enp0s3

16. The conf file is located is at: /etc/sysconfig/network-scripts/ifcnfg-enp0s3

17. The difference between network device and network connection is that the device is the hardware and physical location. The 
    network connection is the settings that are given to this device that could change depending on needs. 

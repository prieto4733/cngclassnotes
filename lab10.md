# Lab 10 

---

1. I learned that ssh is based on static Ip addresses, I came back to finish the lab 
   a day after I configured the /etc/hosts files, and could not connect until I figured
   it out. The thing I wounder is when you connect to a server .. the server for sure will
   have a static IP but the computer I will be using to connect probably will be using DHCP
   meaning that the IP address will be not the same when I connect to that server. I find it
   a pain in the butt that I will not be able to connect to the server because of this issue.
   I will be looking into the solutions there is in the industry.

2. I think one of the benefits of having two servers using ssh between each other is that: one 
   it is easy to back up your files from one server to the next. 2 be able to have two working 
   servers that hold different files for a company and separate the files to server depending on
   the deparments.

3. The command is to scp directory is: scp -r ~/ guest:hostname /plum



# Lab 8 

---


1b. The status of the chronyd in my system is inactive (dead)

1c. Yes, sshd is enabled at system boot

1d. Yes, sshd is running and active

1e. I have 298 units listed in my system

1ei. The command that I used to show static services is: systemctl list-unit-files --type=service | grep static

1eii. Static on a service means that you cannot enable the service but another service can start the static service.

2b. PID number 970 

2c. PID number 4727

2d. PID number 4727

3. The command that stops a service to start from boot is: systemctl disable (service)

4. To check if service starts at boot: systemctl is-enable (service)

5. To check if service is currently running: systemctl is-active (service) or systemctl status (service)

6. Masking accomplishes that a service never starts and its linked to /dev/null because that service may be in conflict with 
   another service. It may be used when you need to have services that are in conflict but needed in production.

7. The command that list all active services is: systemctl list-units --type=service, I have 64 running in my system.


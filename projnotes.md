# Final Project


For my final project I chose project 2 which has to do with cron jobs.
I chose this project becuase it is something that it is used in the 
industry. This project was somewhat tricky to finish. I think the major
problem to have doing this task is having your commands in you scripts 
not run properly and your rederections of standard out and err.

The first thing I did was to touch files: memory.usage, disk-cpu.usage and 
tar.results in bin directory wich is in my home directory. I am doing this 
as my normal user. When I find the commands that I needed for each script, 
I edited the respective files and added the shibang line and added the bash 
script to each one. To the memory.usage, the command will show the memory 
that it is used in the system. For the disk-cpu.usgae, the commands will show 
disk usage and cpu usage and will redirect output to /tmp/disk-cpu.usage.
For tar.results, the command will archive and compress the /etc directory and 
add a time stamp in the end of the name. After adding the commands to each script
I will change the mode in each file using the chmod +x <filename> to make the 
script executable.

Now im done with the scripts and its time to add it to the cron directory. I will
change directories to /etc/cron.d. Before adding the cron times i will change use
to use the root user to have provilage to edit the cron file. After changin user to
root. I will run the command crontab -e inside the /etc/cron.d directory to create 
and edit the time for the commands to execute.

FOr the memory.usage the time to run cron will be */5 * * * 1,3,5 /home/user/bin/memory.usage
for the disk-cpu.usage: */15 * * * 1-5 /home/user/bin/disk-cpu.usage
for the tar.results: 0 0 * * 6 /home/user/bin/tar.results
Save and exit the text editor. To check if the cron jobs are active just run:
crontab -l and this will list the cronjobs that are active. 

You can visit the directories that are created by this scripts and see the output and 
see if everything is working how you wanted and fine tune if you need to. 

## Cron Project

Note: all this will be created as a normal user.. you DONT need to change user to root.. I dont give a fuck what your teacher
says.. do what I say and you will have a happy project number 2.. so fuck all that su shit.. 
---

## Setup

---

Make sure that you have Cron installed in your computer and ready to go. To make sure that you have cron installed.
you can run 

```bash
ls /etc | grep cron 
```

If you have cron installed, you will see a list of cron directories ending in .daily ,weekly ext. 


## Scripts

---

Create a folder in the ~ directory called bin. We will have the scripts saved in this "bin" directory. Touch the files 
called as so:

```bash
touch memory.usage disk-cpu.usage tar.results
```

### memory.usage script

with your text editor of choice, enter memory.usage script.. add this script.. 
Remember to ad the shibang to your scripts. then you will add to the scripts the commands that will be called in the cron
job. For the memory usage we will use this script:

```bash 
#!/bin/bash
	
date >> /tmp/memory.usage && 2>/dev/null 
free -h | grep Mem >> /tmp/memory.usage && 2>/dev/null

```

this script will call the date and free command and will redirect to the folder /tmp/memory.usage and also will redirect 
errors to the /dev/null.

### disk-cpu.usage

This script will be 

```bash
date  >> /tmp/disk-cpu.usage 
df -h >> /tmp/disk-cpu.usage 
top -b -n 1 -d1 | grep "Cpu(s)": >> /tmp/disk-cpu.usage 
```

### tar.results

this script will be 

```bash
tar cvf 
```


## Cron job

to create the cron jobs.. cd to /etc/cron.d  When you are there you will run this command in the terminal:

```bash
crontab -e

```
this will automatically start editing this file with the set text editor. the file should be empty and you will add 
this script: note the # are comments so you dont get confused .. also note that /home/one10zero is my home user... change this 
to your /home/username .. 

```bash
# Memory usage cron

*/5 * * * 1,3,5 /home/one10zero/bin/memory.usage

## Disk CPU usage

*/15 * * * 1-5 /home/one10zero/bin/disk-cpu.usage

## tar.results

O O * * 6 /home/one10zero/bin/tar.results
```
	
Save and exit the text editor.. your terminal should give you a success alert .. to make sure that your cron job is running 
and saved properly .. just run in the command in the /etc/cron.d directory

```bash
crontab -l

```

This will list the cron jobs that are active and ready to execute. and I think you are done

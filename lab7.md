# Lab 7

---

1e. If three jobs and stopped number two (assuming that the jobs are in the background) the only thing that
    I noticed is that jobs number two gets the + sign that makes it the default process. no changes in the PID

4a. When you use the -e flag in the ps command it shows the running processes of all the system and users.
   The -f flag shows the processes related to that tty

4b. For long format use -l flag on ps

1f. The four possible states a process could be in are: stopped, running, sleeping, zombie

5a. Top gives you the information about cpu usage and ram usage of a process

6c. The command was running at 90% cpu usage

6d. The command dd is to convert and copy files, if= is read from file instead of stdin and 
   of= is to write to file instead of stdout it is coping and reading files in the /dev/null and dev/zero. 


## Controlling proccesses

The command: jobs, displays the jobs that the current bash shell is tracking for the session.

The command: fg %jobs#, this brings a job to the foreground

To start a job in the background add the command and in the end a & sign

To start a suspended process running in the background use: bg %job#

The + sign in the process indicates that this is the default process.

The PID process ID, the PPID parent process ID, the PGID is the PID of the process group leader.



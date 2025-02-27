# Lab 12

---

## Bash scripts

```bash

#!/bin/bash
#Daniel Rodriuez
#Bash Scirpt 1

clear
echo
echo "**Script 1"
echo "Your current directory is .."
pwd
echo "You're changing to your parent directory, which is ..."
cd
pwd
echo "You're changing back to the script directory."
cd ~/bin
echo "Here is a listing of your files and directories:"
ls -L

#8. No you cannot executed. It still need to change the mode
#!/bin/bash
#Daniel Rodriguez
#Bash Script 2

clear
echo
echo "**Script 2"
STARTLOCATION=$HOME
FILENAME=script1.bash
echo "Searching for the file named $FILENAME"
echo "in the $STARTLOCATION directory"
find $STARTLOCATION -name $FILENAME

#4.it told me in what home directory and the full path of the file script1.bash
#!/bin/bash
#Daniel Rodriguez
#Bash Sciprt 3

clear
echo
echo "**Script 3"
echo "welcome to the FIND script"
echo -n "enter the location (such as /home) where the search should start "
read STARTLOCATION
echo -n "What is the name of the file to search for? "
read FILENAME
echo "Searching starting for the $FILENAME file in the $STARTLOCATION direcotry"
find $STARTLOCATION -name $FILENAME 2>/dev/null

#8.The script run perfeclty and it did what it suppost to do.
#9.This script finds files for you in any directory.
#!/bin/bash
#Daniel Rodriguez
# Bash Script 4

clear
echo
echo "**Scirpt 4"
echo "Searching for $2 starting in the $1 directory"
find $1 -name $2 2>/dev/null


#6. I see that the input has to be givin with the command to run the script
#   I also see that it does the same like script3 but without interaction.
#7. The difference between 3 and 4 is that there is interaction in 3 and in four you need to give the values of the variables with the initial command.
#!/bin/bash
#Daniel Rodriguez
#Bash Script 5

clear
echo
echo "**Script 5"
echo
echo "1) Display your current directory"
echo "2) Display your home directory"
echo "3) List the contents of your current directory"
echo
read CHOICE
if [ $CHOICE = 1 ]
then
  pwd
fi
if [ $CHOICE = 2 ]
then
  echo $HOME
fi
if [ $CHOICE = 3 ]
then
  ls
fi
echo
echo "Have a great day!"


#3. for the three choices, the output was correct.
#4. when you entered 99 as an input, the script printed an empty line and echoed the last line and exited the script


#!/bin/bash
#Daniel Rodriguez
#Bash Script 6

clear
echo
echo "**Script 6"
echo
echo "1)Display your current directory"
echo "2)Display your home directory"
echo "3)List the contents of your curretn direcotry"
echo 
read CHOICE
case $CHOICE in
1) pwd;;
2) echo $HOME;;
3) ls;;
*) echo "You made an invalid selection";;
esac
echo
echo "Have a great day!"


#4. When you enter 99 as an option it give the error messege and exits the script.
#!/bin/bash
#Daniel ROdriguez
#Bash Script 7 

clear 
echo 
echo "**Scirpt 7"
touch testfile
while cat testfile > /dev/null
do
   echo "exit status code is $1"
   sleep 1
done
echo "You deleted the file: testfile"


#3c. When deleting the testfile in the other opened terminal the script stoped running because the file did not exit anymore.
#!/bin/bash
#Daniel Rodriguez
#Bash Script 8

clear
echo
echo "**SCript 8"
for NUMBER in 10 9 8 7 6 5 4 3 2 1
do 
  echo -n "$NUMBER " 
  sleep 1
done
echo Blast off!


#3. Its starts to count down in the same line and then blast off. 
#5. Nothing changed when runned again 
```

## Outputs of bash scripts


**Script 3
welcome to the FIND script
enter the location (such as /home) where the search should start What is the name of the file to search for? Searching starting for the script2.bash file in the /home direcotry
/home/drod/bin/script2.bash

**Scirpt 4
Searching for script2.bash starting in the /home directory
/home/drod/bin/script2.bash


**Script 5

1) Display your current directory
2) Display your home directory
3) List the contents of your current directory

/home/drod/bin

Have a great day!

**Script 5

1) Display your current directory
2) Display your home directory
3) List the contents of your current directory

/home/drod

Have a great day!

**Script 5

1) Display your current directory
2) Display your home directory
3) List the contents of your current directory

control
killing
output5.txt
script1.bash
script2.bash
script3.bash
script4.bash
script5.bash
script6.bash
script7.bash
script8.bash
ShellScript.txt

Have a great day!

**Script 5

1) Display your current directory
2) Display your home directory
3) List the contents of your current directory


Have a great day!


**Script 6

1)Display your current directory
2)Display your home directory
3)List the contents of your curretn direcotry

/home/drod/bin

Have a great day!

**Script 6

1)Display your current directory
2)Display your home directory
3)List the contents of your curretn direcotry

/home/drod

Have a great day!


**Script 6

1)Display your current directory
2)Display your home directory
3)List the contents of your curretn direcotry

control
killing
output5.txt
output6.txt
script1.bash
script2.bash
script3.bash
script4.bash
script5.bash
script6.bash
script7.bash
script8.bash
ShellScript.txt

Have a great day!

**Script 6

1)Display your current directory
2)Display your home directory
3)List the contents of your curretn direcotry

You made an invalid selection

Have a great day!

**Scirpt 7
exit status code is 
exit status code is 
exit status code is 
exit status code is 
exit status code is 
exit status code is 
exit status code is 
exit status code is 
exit status code is 
exit status code is 
exit status code is 
exit status code is 
exit status code is 
exit status code is 
exit status code is 
exit status code is 
exit status code is 
exit status code is 
exit status code is 
You deleted the file: testfile

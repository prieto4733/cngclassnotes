# Lab 2
---

2. Run cat,head,tail on /etc/group
  b. The difference between cat, head, tail is that cat will
  display the full file in the terminal. Head will display the 
  first 10 lines of the file. Tail will display the last 10
  lines of the file. Also cat will display multiple files content
  at the same time.
  c. In my rhel system there is 70 groups. The command that helped
  me find out the number of lines in the file is:
  
  ``` bash
  cat -n /etc/group

  ```
  This cat command will display the content with lines numbered.

  or

  ``` bash
  wc -l

  ```

  This will give you the number of lines in the file.

3. There are two ways (that I know of) that will help you access
your previous ran terminal commands. The first is by pressing the 
up arrow in your keyboard. This key will display the previous command 
typed and if you keep pressing, the one before the last one.
Another way to see the typed commands is to run the command 'history'
and this command will list the last 100 (depending of you configuration)
commands that you used in the terminal.

4. The command wc will help you count either words, lines, and bytes.

5. Tab completions is very helpful when working with terminal. 
You will activate tab completion by pressing tab x2. Depending 
of the command that you are using tab completion with. It will 
list possible options you have in the directory. For example, lets 
say we type the command ls and tab x2. It will list the possible 
directories that we can navigate to.

**Lab Report 1**
1. cd <br>
   
   a.
   ~~~
   [user@sahara ~]$ cd
   [user@sahara ~]$ 
   ~~~
   The working directory when the command was run was /home <br>
   cd is meant to change directories and does not output anything, however, in this case. we did not specify a directory to move to, and therefore nothing changed <br>
   No error but the directory was not changed. <br>
   
   b.
   ~~~
   [user@sahara ~]$ cd lecture1/messages
   [user@sahara ~/lecture1/messages]$ 
   ~~~
   The working directory when the command was run was /home <br>
   We got that output since we changed to the directory messages by specifying it's path '/lecture1/messages' <br>
   The output was not an error <br>

   c.
   ~~~
   [user@sahara ~]$ cd lecture1/messages/en-us.txt
   bash: cd: lecture1/messages/en-us.txt: Not a directory
   ~~~
   The working directory was /home <br>
   We got that error message since we cannot change directories to a file <br>
   It is an error since it cannot navigate to a file <br>


2. ls <br>
   
   a.
   ~~~
   [user@sahara ~]$ ls
   lecture1
   ~~~
   The working directory was /home <br>
   We got that output since the command ls lists the files/directories in that specific directory <br>
   Not an error <br>
   
   b.
   ~~~
   [user@sahara ~]$ ls lecture1/messages
   en-us.txt  es-mx.txt  nl-be.txt  zh-cn.txt
   ~~~
   The working directory was /home <br>
   We got that output since it listed the files stored under the directory 'messages' <br>
   Not an error <br>
   
   c.
   ~~~
   [user@sahara ~]$ ls lecture1/messages/en-us.txt
   lecture1/messages/en-us.txt
   ~~~
   The working directory was still /home since we navigated to the path but didnt change directories <br>
   We got that output since it just listed the file that we gave the path to, which is en-us.txt <br>
   Not an error, the file was listed as expected after giving it's path <br>


3. cat <br>
   
   a.
   ~~~
   [user@sahara ~]$ cat
   
   ~~~
   The working directory was /home <br>
   We got that output since we did not give the command any files to concatenate <br>
   Not an error but no valid output generated <br>

   b.
   ~~~
   [user@sahara ~]$ cat lecture1/messages
   cat: lecture1/messages: Is a directory
   ~~~
   The working directory was /home <br>
   We got that output to explain that we cannot concatenate a single directory <br>
   An error since we cannot concatenate a single directory <br>
      I tried to find a way to concatenate directories and found the code doing this: <br>
   ~~~
         [user@sahara ~]$ cat lecture1/messages lecture1/README
         cat: lecture1/messages: Is a directory
         To use this program:
         javac Hello.java
         java Hello messages/en-us.txt
   ~~~
      This time the outputd didn't let us concatenate messages but did print the contents of README, so it partially worked. <br>
      
   c.
   ~~~
   [user@sahara ~]$ cat lecture1/messages/en-us.txt lecture1
   /messages/nl-be.txt
   Hello World!
   Hallo Wereld!
   ~~~
   The working directory was /home <br>
   We got the output we wanted since it concatenated the contents of the two .txt files <br>
   Not an error <br>

**Lab Report 1**
1. cd
   
   a.
   ~~~
   [user@sahara ~]$ cd
   [user@sahara ~]$ 
   ~~~
   The working directory when the command was run was /home
   We got that output since cd is meant to change directories, but we did not indicate which directory to change to so we did not receive an output.
   No error but no output was generated.
   
   b.
   ~~~
   [user@sahara ~]$ cd lecture1/messages
   [user@sahara ~/lecture1/messages]$ 
   ~~~
   The working directory when the command was run became /home/lecture1/messages
   We got thae output since we changed to the directory messages by specifying it's path
   The output was not an error

   c.
   ~~~
   [user@sahara ~]$ cd lecture1/messages/en-us.txt
   bash: cd: lecture1/messages/en-us.txt: Not a directory
   ~~~
   The working directory was /home
   We got that output since we cannot change directories to a file
   It is an error since it cannot navigate to a file


2. ls
   
   a.
   ~~~
   [user@sahara ~]$ ls
   lecture1
   ~~~
   The working directory was /home
   We got that output since the command ls lists the files/directories in that specific directory
   Not an error
   
   b.
   ~~~
   [user@sahara ~]$ ls lecture1/messages
   en-us.txt  es-mx.txt  nl-be.txt  zh-cn.txt
   ~~~
   The working directory was /home
   We got that output since it listed the files stored under the directory 'messages'
   Not an error
   
   c.
   ~~~
   [user@sahara ~]$ ls lecture1/messages/en-us.txt
   lecture1/messages/en-us.txt
   ~~~
   The working directory was still /home since we navigated to the path but didnt change directories
   We got that output since it couldn't list any files under the files themselves
   Not an error but no valid output generated


3. cat
   
   a.
   ~~~
   [user@sahara ~]$ cat
   
   ~~~
   The working directory was /home
   We got that output since we did not give the command any files to concatenate
   Not an error but no valid output generated

   b.
   ~~~
   [user@sahara ~]$ cat lecture1/messages
   cat: lecture1/messages: Is a directory
   ~~~
   The working directory was /home
   We got that output to explain that we cannot concatenate a single directory
   An error since we cannot concatenate a single directory
      I tried to find a way to concatenate directories and found the code doing this:
   ~~~
         [user@sahara ~]$ cat lecture1/messages lecture1/README
         cat: lecture1/messages: Is a directory
         To use this program:
         javac Hello.java
         java Hello messages/en-us.txt
   ~~~
      This time the outputd didn't let us concatenate messages but did print the contents of README, so it partially worked.
   c.
   ~~~
   [user@sahara ~]$ cat lecture1/messages/en-us.txt lecture1
   /messages/nl-be.txt
   Hello World!
   Hallo Wereld!
   ~~~
   The working directory was /home
   We got the output we wanted since it concatenated the contents of the two .txt files
   Not an error

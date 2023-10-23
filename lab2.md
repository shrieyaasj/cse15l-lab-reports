**Lab Report 2**
PART 1 <br>

   
   Code for String Sever: <br>
   ~~~
  import java.io.IOException;
  import java.net.URI;
  
  class Handler implements URLHandler {
  
      int num = 0;
  
      public String handleRequest(URI url) {
          if (url.getPath().contains("/add-message")) {
              String[] parameters = url.getQuery().split("=");
              if (parameters[0].equals("s")) {
                  num += 1;
                  return num + "." + parameters[1] + "\n";
              }
              return "404 Not Found!";
          }
          return "";
      }
  }
  
  class StringServer {
      public static void main(String[] args) throws IOException {
          if(args.length == 0){
              System.out.println("Missing port number! Try any number between 1024 to 49151");
              return;
          }
  
          int port = Integer.parseInt(args[0]);
  
          Server.start(port, new Handler());
      }
  }
   ~~~


   1. URLHandler and StringServer methods are called. <br>
   2. The relevant arguments for URLHandler are the string passed in after the =. The value is a string.<br>
   <br>


PART 2 <br>

3.
~~~
[cs15lfa23oe@ieng6-203]:.ssh:28$ cd ~/.ssh/
[cs15lfa23oe@ieng6-203]:.ssh:29$ ls
known_hosts
[cs15lfa23oe@ieng6-203]:.ssh:30$ ls ~/.ssh/known_hosts
/home/linux/ieng6/cs15lfa23/cs15lfa23oe/.ssh/known_hosts
~~~

PART 3


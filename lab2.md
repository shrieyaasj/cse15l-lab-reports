**Lab Report 2** <br>
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
                return (num + ". " + parameters[1] + "\n");
            }
            return "404 Not Found!";
        }
        return "";
    }
}

public class StringServer {
    public static void main(String[] args) throws IOException {
        if (args.length == 0) {
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);
        Server.start(port, new Handler());
    }
}

   ~~~
![Image](ss1.png) <br>

   1. URLHandler and StringServer methods are called. <br>
   2. The relevant arguments for URLHandler are the string passed in after the = and gets stored in parameters (for eg, parameters[1] is "How are you". The value is a string.<br>
   3. The field num is being incremented by 1 as and when a new string is added. <br>
<br>

![Image](ss2.png) <br>


   1. URLHandler and StringServer methods are called. <br>
   2. The relevant arguments for URLHandler are the string passed in after the = and gets stored in parameters (for eg, parameters[1] is "How are you". The value is a string.<br>
   3. The field num is being incremented by 1 as and when a new string is added. <br>
<br>


PART 2 <br>
1. 
~~~
C:\Users\shrie/.ssh/id_rsa
~~~

2.
~~~
C:\Users\shrie/.ssh/id_rsa.pub
~~~

3. 
![Image](q3lab2.png) <br>

<br>

PART 3 <br>
I can login to my ucsd server without needing a password every single time on my local computer
<br>


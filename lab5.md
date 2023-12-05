
**Lab Report 5** <br>
PART 1 <be>
1. Hi i'm having trouble obtaining the right output for my factorial program. PFA below my screenshot for errors
2. Hi I see that the for loop that you have currently starts by initializing with 1. If you could try initializing with 2 instead and check if that helps anyway?


File and directory structure:
project/
 - FactorialCalculator.java
 - FactorialTests.java
 - tests.sh

FactorialCalculator.java
~~~
public class FactorialCalculator {
    public static long calculateFactorial(int number) {
        long factorial = 1;

        for (int i = 2; i <= number; ++i) {
            factorial *= i;
        }

        return factorial;
    }
}
~~~
FactorialTests.java
~~~
import static org.junit.Assert.*;
import org.junit.*;
import java.util.*;



public class FactorialCalculatorTest {

    @Test
    public void testFactorialInput5() {
        assertEquals(120, FactorialCalculator.calculateFactorial(5));
    }

    @Test
    public void testFactorialInput10() {
        assertEquals(3628800, FactorialCalculator.calculateFactorial(10));
    }
}
~~~
tests.java
~~~
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore FactorialTests.java
~~~

PART 2 <br>
I thought designing our own autograder was super interesting since I now have a base-level understanding of what happens when I submit assignments. Especially when it came to using bash scripts to navigate through the directory and outputs to then print error/success messages. It took my knowledge of writing junit tests to another level. I found all the ways to traverse through files ery interesting using the bash scripts.

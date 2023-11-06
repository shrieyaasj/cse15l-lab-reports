**Lab Report 3** <br>
PART 1 <br>
Choosing the revered method to test:
<br>

1. Failure-inducing input <br>

~~~
@Test
  public void testReversed() {
    int[] input = {1,2,3,4};
    int[] expected = {4,3,2,1};
    assertArrayEquals(expected,ArrayExamples.reversed(input));
  }
~~~
<br>
2. Input that does not induce Failure <br>

~~~
@Test
    public void testReversedNoFailure() {
        int[] input = {5, 10, 15, 20};
        int[] expected = {0,0,0,0};
        assertArrayEquals(expected, ArrayExamples.reversed(input));
    }
~~~
<br>
3. Symptom <br>

![Image](lab3symptom.png)


<br>




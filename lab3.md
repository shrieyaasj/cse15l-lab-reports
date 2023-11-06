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

4. Before and After <br>

before: <br>

~~~
static int[] reversed(int[] arr) {
  int[] newArray = new int[arr.length];
  for(int i = 0; i < arr.length; i += 1) {
    arr[i] = newArray[arr.length - i - 1]; //this is the buggy line
  }
  return arr;
}
~~~
<br>
after: <br>

~~~
static int[] reversed(int[] arr) {
  int[] newArray = new int[arr.length];
  for(int i = 0; i < arr.length; i += 1) {
    newArray[i] = arr[arr.length - i - 1]; //this is the fixed line
  }
  return arr;
}
~~~
<br>

The reason why this code change works is because now the values from the original 'arr' are assigned to 'newArray' and therefore there's a place to store the contents from the original array to be able to continue reversing the rest of the array.



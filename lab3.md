# Lab Report 3

---
**Part 1:**

1. A failing test:
  ~~~
  @Test
  public void failTestAverageWithoutLowest() {
    double[] input1 = {1,1,2,3};
    assertEquals(2.0, ArrayExamples.averageWithoutLowest(input1),0.000001);
  }
  ~~~
  Symptom:
![Image](FailurSymptom.png)

2. A passing test:
  ~~~
  @Test
  public void passTestAverageWithoutLowest() {
    double[] input1 = {1,2,3,4};
    assertEquals(3.0, ArrayExamples.averageWithoutLowest(input1),0.000001);
  }
  ~~~
  Symptom:
  ![Image](PassSymptom.png)

3. Problematic Function:
      ~~~
     static double averageWithoutLowest(double[] arr) {
    if(arr.length < 2) { return 0.0; }
    double lowest = arr[0];
    for(double num: arr) {
      if(num < lowest) { lowest = num; }
    }
    double sum = 0;
    for(double num: arr) {
      if(num != lowest) { sum += num; }
    }
    return sum / (arr.length - 1);
   }
  ~~~
4. Fixed Function:
   ~~~
  static double averageWithoutLowest(double[] arr) {
    if(arr.length < 2) { return 0.0; }
    double lowest = arr[0];
    for(double num: arr) {
      if(num < lowest) { lowest = num; }
    }
    double sum = 0;
    for(double num: arr) {
      sum += num; 
    }
    sum -= lowest;
    return sum / (arr.length - 1);
  }
  ~~~


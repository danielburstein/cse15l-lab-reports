# Lab Report 3

---
**Part 1:**

1. A failure-inducing:
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

---
Second /add-message:

![Image](Lab2Pic3.png)

1. Methods:
2. Arguments and Values:
3. Change:
   
---

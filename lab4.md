# Lab Report 4

---
**STEP 1**

1. Log into ieng6:
   
   Command: ``` ssh cs15lfa23by@ieng6.ucsd.ed ```  \<enter\>
   Result:
   ![Image](Lab4_Pic1.png)
   Summary: Running this command would connect and log you into the remote ieng6 server.
   
2. Clone your fork :

   Locate the URL:
   ![Image](Lab4_Pic2.png)
   Command: ``` ssh cs15lfa23by@ieng6.ucsd.ed ```  \<enter\>
   Result:
   ![Image](Lab4_Pic3.png)
   Summary: Running this command would connect and log you into the remote ieng6 server.

4. Problematic Function:
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
5. How it is fixed:
The problematic function failed in the situation when multiple numbers in the array were the lowest. For example, if the array was {1,1,3} it should remove only one of the ones which would give you an average of 2 but the problematic function ends up removing both the ones and returning an average of 3. This happened in the line `if(num != lowest) { sum += num; }` this check happens every time it wants to add any number to the sum but it doesn't take into account if 2 or more of the same number are the lowest. To fix this function I ended up removing the if statement which just adds all of the numbers together and then I just subtracted the lowest value one time at the end.

---



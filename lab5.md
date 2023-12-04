# Lab Report 5

---

**Part 1**

---

**Student Post**:
   
   > Hey, I am having trouble figuring out what is wrong. I am currently working on lab3 and when I run
   > the command `bash test.sh` into the terminal it is giving me a really big error. This is what it shows me:
   
   ![Image](Lab5_Pic1.png)
   
   > I think I might have done something wrong in my "test.sh" or in my "ArrayTests.java" file
   > These are the images for what are in those files:

   ![Image](Lab5_Pic2.png)

   ![Image](Lab5_Pic3.png)

**TA Response**:

  > Hey, `Student` I see that you are getting an error when you run that bash command. Based on the output
  > in the terminal it seems like this isn't coming from your test.sh file but rather one of your   
  > assertions are failing. Specifically in the "failTestAverageWithoutLowest" function in your       
  > ArrayTests.java file. This means that when you ran averageWithoutLowest(input1) in that function the
  > output was not "2.0". So there seems to be a problem in your averageWithoutLowest function. I hope   
  > that helps!    

**Student Response**:

  > I went ahead and re checked my averageWithoutLowest function and you were right, I ended up not   
  > creating that function in the way that I wanted so it gave me the wrong result when I ran it.
  > I went ahead and changed that function and now when I run the command `bash test.sh` it all works.

  ![Image](Lab5_Pic4.png)

  > Thank you soo much for your help!
   

   

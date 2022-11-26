#  Lab report 5: by Christophian Austin Sulaiman
```
temp=student-grade/
rm -rf student-submission
rm -rf $temp
git clone $1 student-submission
CP=.:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar
mkdir $temp
cp ./student-submission/ListExamples.java $temp
cp TestListExamples.java $temp
cp -r lib $temp
cd $temp

javac -cp $CP *.java
java -cp $CP org.junit.runner.JUnitCore TestListExamples.java 2> error-output.txt

javac ListExamples.java

if [ $? -eq 0 ];
 then
    echo "It was a success"
else
    echo "It was a failure"
fi
```

**Images of the three localhost**

![Alt text](../../../../../../C:/Users/Christophian%20S/Documents/GitHub/cse15l-lab-reports/phian%2011.png)

![Alt text](../../../../../../C:/Users/Christophian%20S/Documents/GitHub/cse15l-lab-reports/phian%2022.png)

![Alt text](../../../../../../C:/Users/Christophian%20S/Documents/GitHub/cse15l-lab-reports/phian%2033.png)


I will be tracing the script for the first image out of the three above:



For the first link that I've used, the rm file will remove that directory or file for every time the grade.sh is used. So everytime, there will be a new student-submission and student-grade/. This stage, there are no errors and the exit code would be 0. For the git clone command there are no errors, hence a 0 exit code. For my program, I used two variables, temp and CP, as in class path. The standard output for the git clone command is "Cloning into 'student-submission'...".  There are no errors present for the clone command. mkdir temp, or in this case mkdir student-grade/ will create a new directory student-grade/ for usage for the code. The cp commands that I use for the next 4 lines of code will copy files or directories, and if successful will return an exit code of 0. 

The javac and java command will compile and execute the JUnit program. For my code, it all ran smoothly, with no errors. While executing the java command, there is a error re-direction, or error-output.txt, however since it ran smoothly we did not see it. Then we compile ListExamples.java. The standard outputs given by the program are :
```
JUnit version 4.13.2
.E
Time: 0.115
There was 1 failure:
1) testTimeout(TestListExamples)
org.junit.runners.model.TestTimedOutException: test timed out after 100 milliseconds
        at TestListExamples.testTimeout(TestListExamples.java:7)

FAILURES!!!
Tests run: 1,  Failures: 1
```
There are no standard errors in the file error-output.txt, everything ran smoothly. Next, the if statement will determine the statements being prints. If the exit code is a 0, then it will give a standard output, or print "It was a success", any other number than a 0, is a failure and will give a standard output or print "It was a failure".
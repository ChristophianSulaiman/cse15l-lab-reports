#  Lab report 5: by Christophian Austin Sulaiman
```
# Create your grading script here
FILE='ListExamples.java'
rm -rf student-submission
git clone $1 student-submission
echo 'Finished cloning'

cd student-submission
if [ -f $FILE ]
then
    echo "Found the file!"
else
    echo "Could not find the file!"
    echo "The grade is 0%"
    exit 1
fi

cp ../TestListExamples.java .

javac -cp .:../lib/hamcrest-core-1.3.jar:../lib/junit-4.13.2.jar *.java 2> out-error.txt

if [ $? -eq 0 ]
then
    echo "Compiled successfully"
else
    echo "Compile failed"
    cat out-error.txt
    echo "Grade received is 0%"
    exit 1
fi


java -cp .:../lib/hamcrest-core-1.3.jar:../lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples > test-result.txt


if [ $? -eq 0 ]
then
    echo "JUnit results for the tests are below:"
    cat test-result.txt
    echo "Grade: 100%"
else
    echo "JUnit results for the tests are below:"
    cat test-result.txt
    echo "Grade: 50%"
    exit 1
fi
```

**Images of the three localhost**

![Alt text](../../../../../../C:/Users/Christophian%20S/Documents/GitHub/cse15l-lab-reports/cse15l%20first.jpg)

![Alt text](../../../../../../C:/Users/Christophian%20S/Documents/GitHub/cse15l-lab-reports/cse15l%20second.png)

![Alt text](../../../../../../C:/Users/Christophian%20S/Documents/GitHub/cse15l-lab-reports/phian%20ss3.png)

I will be tracing the script for the second image out of the three above:

Firstly. I'd like to mention that I did not use a variable to store the command for compiling, which could have been done to enhance the program's efficiency. I started off by creating a FILE variable for ListExamples.java. Then the rm command will remove the directory student-submission if it already exists since we may run the code more than once, which was a success with an exit code of 0. Next, I git cloned the link that the user will provide into the directory student-submission, and I printed "Finished cloning" after the git clone ran successfully for this trace. 

I then moved working directory to student-submission using the cd command, and then for the first if statement, we searched if the FILE exists, if it does then "Found the file!" is printed and the exit code remains 0 (correct), otherwise an error output is printed and that the grade is 0%, along with an error code of 1 which indicates an error. The file does exist for this tracing, and so it ran smoothly without an exit code that isn't a 0. 

Next we cp, which ran successfully, and then we compiled every java file and if an error occurs, we re-direct the error into out-error.txt. For the if statement, we check whether or not the value is a 0 or otherwise, if 0 it is a success, and will print out that it compiled successfully, otherwise will print compile failed and will give the contents of the error text file and will give an exit code of 1, which represents an error. In this case, this step was a success with an exit code of 0 and the contents of out-error.txt has been updated. 

Next we ran TestListExamples and redirect output to test-result.txt. Then another if statement, if the value of $? is a 0, then it will print that the JUnit results are the contents of the test-results.txt, which we redirected before, and that everything is successful with a grade 100%. otherwise then the code will get a 50% grade and an exit code of 1. For the trace that we are doing, the value is a 0, hence gotten a grade of 100%, and the exit code remains a 0 which is a success.

```
Cloning into 'student-submission'...
Finished cloning
Found the file!
Compiled successfully
JUnit results for the tests are below:
JUnit version 4.13.2
..
Time: 0.021

OK (2 tests)

Grade: 100%
```
Everything ran smoothly and the file out-error.txt is empty. The standard output has an exit code of 0, which indicates that everything ran smoothly. Everything printed indicates all ran smoothly, and that for the last 2 if statements, the trace runs the first condition for both.

[def]: ../../../Desktop/cse15l%20third.png
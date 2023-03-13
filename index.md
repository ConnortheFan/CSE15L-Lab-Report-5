# Grading Script

![Screenshot 2023-03-12 232128](https://user-images.githubusercontent.com/110417453/224623179-b39d635e-4bc5-49a5-9c8a-05b815e4633f.png)
![Screenshot 2023-03-12 232149](https://user-images.githubusercontent.com/110417453/224623351-530cb9fe-7af1-4fd9-8acf-1435dc2235ec.png)
![Screenshot 2023-03-12 232204](https://user-images.githubusercontent.com/110417453/224623410-d3d8a1da-44cb-4f0d-ac69-71f619cfa0a7.png)

This grading script was made in collaboration by me and my partner Alon. The different CPATH's on lines 1 and 2 are the result of running the grading script on different operating systems. If this script were to be used on a LINUX/MAC environment, like the ieng6 remote server, then the first CPATH should be used, but on a WINDOWS environment, use the second CPATH. 

Lines 4-8 were initially made to tell the user if they forgot to include an argument and just ran `bash grade.sh`. However, we found this unnecessary because the code would report a bug anyways.

Line 10 removes the previous student submission, so the grade script runs on a fresh slate every time.

Lines 11-12 clone the github repository into a folder called `student-submission`, and report if the cloning was finished.

Lines 14-20 check if the correct files exist by using the `-e` command, which check for existing files.

Lines 22-24 copy over all necessary resources into the `student-submission` file and then moved the current directory to `student-submission`.

Line 26 sets the option to stop the command when encountering an error.

Lines 27-35 compile the code and report whether it was successful.

Line 37 runs the tests and puts it into test-results.txt

Line 39 formats the terminal to show the results of the test.

Lines 44-46 create color variables, for nicer looking output.

Lines 48-50 check for an OK test result, with no tests failing.

Lines 53-64 check if there were any failed tests, and display which ones failed.

## list-methods-lab3

![image](https://user-images.githubusercontent.com/110417453/224623603-5d701e85-5ff6-4668-a042-cac4a74a456f.png)

This code is the same as the starter code, and and therefore should fail some tests due to not having implementation. As seen, it displays the correct result, although it doesn't show which test failed, which may be a bug.

## list-methods-corrected

![image](https://user-images.githubusercontent.com/110417453/224623785-54e38c69-2d40-4e6d-b601-871721c51b35.png)

This code has correct implementation, and displays that all tests passed, which is expected.

## list-methods-compile-error

![image](https://user-images.githubusercontent.com/110417453/224623904-a58a4147-f1c3-4e07-970c-cf9519da3af8.png)

This code has a syntax error of a missing semicolon, so it isn't expected to compile, which is shown in the output when it says, `Failed to compile` as well as the location of the error.

## list-methods-signiature

![image](https://user-images.githubusercontent.com/110417453/224624068-fff31a66-28d2-4edf-bfc0-fcd5d1aaf004.png)

This code has the arguments of `filter` in the wrong order, so it doesn't match the expected behavior. However, it passed all tests, which is a sign that somewhere the grade script could be improved to check for this. Perhaps, by checking for certain lines within the code, could it search for incorrect method signatures.

## list-methods-filename

![image](https://user-images.githubusercontent.com/110417453/224624144-c86fe5ea-447b-4d18-b73d-abc3a6127511.png)

This code has great implementation in a file with the wrong name. It is expected that since the name is incorrect, the grader should report that it is unable to find the file, which it correctly does.

## list-methods-nested

![image](https://user-images.githubusercontent.com/110417453/224624228-a48b8243-8be9-43db-ae6a-e24721ef180a.png)

This code has great implementation in a nested directory called `pa1`. Since the code is in a nested directory, the student clearly did not follow instructions for submitting their assignment, therefore I expect the grading script to report that it couldn't find the file, which it properly does.

## list-examples-subtle

![image](https://user-images.githubusercontent.com/110417453/224624327-afc9566b-00b0-4d8b-98e1-8fdb85e48531.png)

This code has more subtle bugs, like using `==` instead of `.equals()`. However, since it only needs to compare to the tests, it should still fail the proper tests and display the correct output, which it does.

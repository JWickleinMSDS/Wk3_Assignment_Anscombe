***Instructions:*** 

1) Execute the "anscombe_data.R" file from the terminal using the command "Rscript anscombe_data.R".  Once executed, the execution time will be recorded in the file "R_execution_time.txt".

2) Execute the "anscombe_data.py" file from the terminal using the command "python anscombe_data.py".  Once executed, the execution time will be recorded in the file "Python_execution_time.txt".

3) Execute the "anscombe_data.go" file from the terminal using the command "go run anscombe_data.go".  Once executed, the execution time will be recorded in the file "Go_execution_Time.txt".  Additionally, the output displayed in the terminal will include the linear regression coefficients for each of the four pairings.  Further, these results are recorded to the file "Go_linreg_output.txt".

4) Execute the "anscombe_data_test.go" file from teh terminal using the command "go test".  The file will collect the execution times from the Go, Python, and R execution time files and display them in the output within the terminal.  Secondly, it will grab the linear regression coefficients from the "anscombe_data.go" file and compare them to the linear regression coefficients that were produced by the anscombe code in the Python and R code. If the results match (with an allowance for rounding) the test will pass.  

***Notes:***  
- In the "anscombe_data.py" and "anscombe_data.R" files the code began as a copy of what was provided in the assignment.  Two changes were made, though.  First, any charts or pdfs were commented out.  Second, code was inserted to record the execution times of each. 
- In the file "anscombe_data.go" the values for the linear regression coefficients from the R code, which are nearly identical to those within the Python code, were hard coded.
- I attempted to leverage Montana Flynn within the Go code.  I was able to find an example that calculated linear regression outputs, however, it's values failed to produce the expected result.  Accordingly, I shifted to the "math" library to determine the linear regression coefficients in Go.  That library produced the desired outcomes.  

***Note to management:***

Based on the tests conducted the linear regression coefficients from the Anscombe pairings could be easily reproduced in Go using the "Math", and other, libraries. Further, the results matched what was produced in Python and R. 

Execution time for Anscombe within Go was longer than that of Python or R, possibly attributed to somewhat suboptimal Go code written on my behalf.  That said, the execution times were still fast (~1 millisecond). 

There are a couple potential challenges with respect to using the Go statistics package instead of Python or R statistical packages.  First, there are likely more library choices with Python or R than Go.  Secondly, it may be more challenging to find resources (personnel) with prior Go experience.  Lastly, visualization packages and libraries may be more abundant in Python or R.
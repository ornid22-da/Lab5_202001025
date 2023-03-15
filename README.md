# Lab5_202001025
## Lab 5 - Static Analysis

### Static Analysis Tool
Static analysis is a method of examining the source code of a software program without executing it. Static analysis can help detect errors, bugs, vulnerabilities, and other quality issues in the code. Static analysis tools can perform various tasks such as checking syntax, style, logic, data flow, control flow, and security. Static analysis can improve the reliability, performance, and maintainability of software by identifying and correcting defects early in the development process.

**Static Analysis Tool Used:** Pylint. It has a number of features, from coding standards compliance to bug detection, and helps with refactoring (by detecting duplicate or unused code).    
**Command to Install Pylint:** python -m pip install pylint   
**Command to Run Pylint on any Python File:** pylint app.py   

Note that Pylint prefixes each of the problem areas with an R, C, W, E, or F, meaning:   
[R] - Refactor for "good practice" metric violation  
[C] - Convention for coding standard violation  
[W] - Warning for stylistic problems, or minor programming issues  
[E] - Error for important programming issues (i.e. most probably a bug)  
[F] - Fatal for errors which prevented further processing


### Screenshot of Code Lines having errors
![Screenshot 2023-03-15 151248](https://user-images.githubusercontent.com/122976431/225270470-1842edec-83b6-4531-995a-2d990b37ebb6.png)

        
### Screenshot of Errors found
![Screenshot 2023-03-15 150044](https://user-images.githubusercontent.com/122976431/225268454-af5a340f-6725-4e28-b4cc-3f2c80c2eab2.png)

In the lines 15,16,17 and 18 errors of the kind "Doesn't conform to UPPER_CASE naming style (invalid-name)." This error is True Positive as the code is not contained in a class or function it is expecting those variables to be constants and as such they should be uppercase.   

In the line 21 error of the kind "Missing Function or Method Docstring (method-function-docstring)." This error is True Positive as the code file is missing a module docstring which should be added at the starting of a file.   

In the lines 29 and 35 error of the kind "Using open without explicitly specifying an encoding (unspecified-encoding)". This error is True Positive as the code file does not mention the encoding. Using the system default implicitly can create problems on other operating systems.  

### Github Repo: Website Blocker Python
Github Repo Link: https://github.com/Kalebu/Website-blocker-python

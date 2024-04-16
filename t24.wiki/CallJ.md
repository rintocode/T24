# Call Java Class Method from Infobasic(T24)

## Create a java program
Use the code editor or IDE such as IntelliJ or Eclipse
## Create jar file
1. Navigate to your project folder
2. Compile source code `$ javac *.java` 
3. Create a manifest file `$ echo Main-Class: Main > manifest.txt`   
4. Create Jar file: `$ jar cvfm [jarname].jar manifest.txt *.class`
5. Test your jar: `$ java -jar [jarname]`
## Create infobasic proram

### Syntax
`CALLJ class_name, [$]method_name, param SETTING ret [ON ERROR] err_statement` 

### Basic Sample:

``` basic
0001  PROGRAM TestCallJ
0002
0003     class_name = "io.mathisi.test.Greeting"
0004     method_name = "hello"
0005     param = "Aaron"
0006
0007     CALLJ class_name, method_name, param SETTING ret ON ERROR
0008         err = SYSTEM(0)
0009         CRT "Error code ": err
0010         RETURN
0011     END
0012
0013     CRT "Received from Java": ret 
0014
0015 END
```
### Errors

|Code  |Description
|------|-----------------------------
| 1    |   Fatal error creating thread
| 2    |  Cannot create JVM
| 3    |  Cannot find class
| 4    |  Unicode conversion error
| 5    |  Cannot find method
| 6    |  Cannot find object constructor
| 7    |  Cannot instantiate object
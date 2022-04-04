1. The logger.log and console is different because in the file, it specifies that the level sent to the file should be ALL, while the level sent to the console should be INFO. This filters out the messages sent depending on if it is the file or the console.
2. The message appears because the function public TimerException(String message) was not overridden with the logger command "Disabled".
3. AssertThrows asserts that a timer exception was thrown when the call to the function was made. Some invalid input was fed into our function, so our function handled this invalid input correctly.
4. 
    1. It is a unique identifier for each class. It ensures that the same class was used during Serialization is loaded during Deserialization.
    2. The constructors are overridden because it is passed a unique message so we can call a specific exception that deals specifically with the timer class. It needs to generate its own object through inheritance and use other methods from exception. 
    3. Other exception classes are simply inherited from the exception parent, therefore we do not have to override them.
5. It tries to configure the logger in order to generate its report based on the files specifications. The static block is run first. 
6. The format is ordered list format because is goes in ascending order for each point.
7. It is failing because the assertThrows expects a timer exception, but instead it is getting a nullptr exception. This is due to the variable being called "timeNow" being set to null, then trying to subtract that from the current time as part of the logger. I fixed this my just setting time now to the current system time
8. The actual issue is that it throws the exception for the timer, then it continues to try to solve a math problem, but it cannot because it is a null value, so then it overrides the exception from timer to nullpointer. An actual issue here is that the timerException does not stop the function. 
9. picture
10. picture
11. The timer exception and nullpointer exception are both unchecked as there are no catch blocks for these errors. They are also both runtime exceptions as they are only caught after the program has been run. 
12. push
# How-to-rest-the-TCP-Port-in-Windows

To reset a TCP port that is listening on 0.0.0.0:2000, you can follow these general steps:

   Identify the process associated with the port: Open the command prompt or terminal on your system and run the following command:
   ```python

   netstat -ano 
   ```
![image](https://github.com/Goldu/How-to-rest-the-TCP-Port-in-Windows/assets/26148152/55c94b87-e7be-458b-a0d4-e515bbb930f5)

if you don't find the PID id of your port no, you can use this command to find the PID. This will display the process ID (PID) of the program using the port.
   ```python

   netstat -ano | findstr :port_no
   ```
Example
```python

   netstat -ano | findstr :2000
   ```
![image](https://github.com/Goldu/How-to-rest-the-TCP-Port-in-Windows/assets/26148152/cb4b1463-3670-4349-a638-ad8e6f1dd85a)


## Terminate the process: 
Use the PID obtained from the previous step to stop the program or process using the port. In the command prompt or terminal, execute the following command:
Example
```python

   taskkill /PID <PID> /F
Replace <PID> with the actual process ID you obtained.
   ```
## Verify that the port is no longer in use:
Run the netstat command again to ensure that the port is no longer listed. Use the command:
```python

   netstat -ano | findstr :2000
   ```
If the port is no longer in use, there should be no output.

##### Note: At this point, the port should be reset and available for use. 
If you're intending to use the port for a specific program or service, make sure to restart that program after resetting the port.

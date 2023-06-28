# How-to-rest-the-TCP-Port-in-Windows

## To reset a TCP port that is listening on 0.0.0.0:2000, you can follow these general steps:

   Identify the process associated with the port: Open the command prompt or terminal on your system and run the following command:
   ```python

   netstat -ano | findstr :port_no
   ```
if you don't find the PID id of your port no, you can use this command to find the PID
   ```python

   netstat -ano | findstr :port_no
   ```
Example
```python

   netstat -ano | findstr :2000
   ```

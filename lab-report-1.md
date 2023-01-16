#Installing VS Code
![VS code setup screenshot](assets/cse15l-lab_report1_ss1.png)

I already had VS Code installed as I took CSE11 last quarter, so I could skip this step. However, if I had to reinstall it, I would go to https://code.visualstudio.com/download and download the installer for windows.

#Remotely Connecting 
![Remote Connection screenshot 1](assets/cse15l-lab_report1_ss2.png)

First I downloaded Git for Windows from https://gitforwindows.org/, selecting VS Code as my default text editor. Then I opened a terminal in VS Code and inputted the following command:
```
$ ssh cs15lwi23ask@ieng6.ucsd.edu
```

Note that I do not need to type in the $ into the terminal.


![Remote Connection screenshot 2](assets/cse15l-lab_report1_ss2point5.png)
Then, I typed "yes" to continue connecting. Note that this should only happen once and not everytime I try to connect, as it might indicate somebody else is snooping.

![Remote Connection screenshot 3](assets/cse15l-lab_report1_ss3.png)
When I successfuly connected remotely, the cluster status was displayed. Also, I was able to now pass in commands.

![Trying commands screenshot](assets/cse15l-lab_report1_ss4.png)
Now I tried using various commands, including the ls and ls -lat command. To close the connection, I can use the exit command.

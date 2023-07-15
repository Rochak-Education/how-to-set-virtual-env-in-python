
# How To Create A Virtual Environment in Python and How to Fix the error while activating the script  

This repository will help you to create a virtual environment as well it will also help you deal with error which will occur while creating a virtual env 


# Commands to make Virtual Environment 

To start or init the virtual environment just type 
```
python -m venv name_of_environment_you_want
```
In my case I have used the following command 

```
PS C:\Users\Name_of_PC\location_where_file_is_been_stored> python -m venv myenv
```
Once the command completes, you will find a new directory named myenv (or the name you chose) in your current location. This directory contains the virtual environment files and directories.

To activate the virtual environment, run the appropriate command based on your operating system:

⁙For Windows:
```
myenv\Scripts\activate
```
or 

```
name_of_environment_you_want\Scripts\activate
```

⁙For MacOS:

```
source myenv/bin/activate
```

After activation, you should see the virtual environment's name displayed in your command-line prompt.

#

To exit the virtual environment, simply run the following command:

```
deactivate
```

#

By creating a virtual environment, you can maintain isolated Python environments for different projects, each with its own set of installed packages and dependencies.
# Fixing Error For Windows User While Activating Virtual Environment

In some case You will encounter this Error Message: 



![App Screenshot](https://i.ibb.co/N1TXVZb/error.png)


"Activate.ps1 cannot be loaded because running scripts is disabled on this system,"

This means that the execution of PowerShell scripts is currently disabled on your system.

To solve this issue, you can enable PowerShell script execution by following these steps:

### 1. Open the Start menu on your Windows 10/11 system.
→ Type "PowerShell" in the search bar, and right-click on the "Windows PowerShell" result.

Select "Run as administrator" from the context menu. This will open an elevated PowerShell window with administrative privileges.

→In the PowerShell window, execute the following command to check the current execution policy:

```
get-executionpolicy
```

→ If the current execution policy is set to "Restricted," which is preventing script execution, you can enable script execution by executing the following command:



![Screenshot ](https://i.ibb.co/NKkLkcV/step1.png)
```
set-executionpolicy remotesigned
```



→ PowerShell will prompt you to confirm the change. Type "A" and press Enter to confirm the change.


![Screenshot](https://i.ibb.co/kDJWp1z/step2.png)
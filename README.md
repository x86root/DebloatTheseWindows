  # DebloatTheseWindows by x86Root / Trevor Belt 2025

  # Project Description
Removes basic apps that are installed by default with Windows. Created with modularity in mind for the user to be able to customize however it best fits them. It is built using an array of strings which reference specific apps that are considered "bloatware". Array is very straightforward made with the intention of providing an easy way for users to add/remove any apps they want to include. 
It then loops through each element of the array using a for each loop, catching any errors that may appear.

All of this is logged via Start/Stop-Transcript and output to a text file for the user to review. This location can also be easily modified, making it easy for a user to see that an app is removed that they perhaps didn't intend and can then reinstall.
  Current default path: USERPROFILE\Documents\DebloatLog_$timestamp.txt

Script works directly with Powershell due to certain apps not being able to deleted through the Windows GUI. I know this can be hard for non-computer people and as such I intended something that is a simple download and run.

# Common Bug Fixes
Ensure proper Execution Policy is set: 
  When first running this, most Windows systems will produce an error similar to: "\script.ps1 : File .\script.ps1 cannot be loaded. The file .\script.ps1 is not digitally signed"
  With this, copy this command into Powershell while running as an administrator: 
              Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy Unrestricted
  This allows unsigned scripts(not created on the local system) to be run. Unrestricted still asks for you to confirm you want to run this script. It is written with -Scope to signify to the system that this policy is only for this current session of Powershell. Your security will remain how it was before the command.

# User Setup
  Download and unzip (if needed). Double click the file "debloat_these_windows2.0.ps1" and it will should ask you to confirm you 

# Future Goals: 



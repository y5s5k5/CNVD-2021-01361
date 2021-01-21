Experimental environment: win10 x64    
Software official website:https://www.ijinshan.com    
Software version:9.3.368006   
Affected Component: Kingsoft Antivirus     
  
The root cause of this vulnerability is that ordinary users can open Kingsoft Antivirus software and construct a malicious sample. After being deleted by Kingsoft Antivirus software, they can open the recovery area and restore the sample. However, when Kingsoft Antivirus software restores the sample, if the directory where the sample was deleted does not exist. The user will be allowed to specify any directory to restore. When restoring, it is not judged whether the restored directory has write permission for the current user, resulting in the restoration to C:\Windows\System32 to achieve local privilege escalation   
Before 19h1, any suffix file can be loaded by Diagnostics Hub Service to achieve local privilege escalation.      
Before 19h2, you can use the dui'xiang manager and directory link to create WindowsCoreDeviceInfo.dll. Finally, the Update Session Orchestrator service will execute      WindowsCoreDeviceInfo.dll    

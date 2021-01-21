Experimental environment: win10 x64    
Software official website:https://www.ijinshan.com
Software version:9.3.368006
Affected Component: Kingsoft Antivirus   
  
The root cause of this vulnerability is that ordinary users can open Kingsoft Antivirus and construct a malicious sample. After being deleted by Kingsoft Antivirus, they can open the recovery area and restore the sample. However, Kingsoft Antivirus did not determine the file analysis point and did not use it when restoring the sample. The simulation token also failed to determine whether the target file has write permission during the recovery, so that the symbolic link can be used to recover to C:\Windows\System32 during the recovery, resulting in a local privilege escalation

# SecurityPolicies

To Access Domain Level Password Complexity, Password History, Maximum Password Age & Minimum Password Length

Group Policy MMG > Domains > cybersecurity.local (right click edit) > Computer Configuration > 
Policies > Windows Settings > Security Settings > Account Policies


To Access Renaming Administrator and Guest AccountsEnable the “Do Not Require CTRL + ALT + DEL” logon setting and create legal disclaimer logon banner:

Group Policy MMG > Domains > cybersecurity.local (right click edit) > Computer Configuration > Policies > Windows Settings > Security Settings > Local Policies > Security Options


•	Some Key Policies:
o	Interactive Logon: Message TEXT
o	Interactive Logon: Message TITLE
o	Interactive Logon: Enable the “Do not require….”
o	Account: Rename Administrator
o	Account: Rename Guest


Disable Administrative Shares
Start > Run > type “regedit” (click ok) > HKEY_LOCAL_MACHINE > SYSTEM > CurrentControlSet > Services > LanmanServer > Parameters > AutoShareServer** > Right-Click Edit > Modify > Value Data > 0 > Ok


**If AutoShareServer is not there, then it must be created. Right Click (in free space) > New > REG_DWORD > name AutoShareServer
Exit Registory Editor


Start > Run > cmd (administrative rights) > enter at Command Prompt: net stop server > then enter: net start server > exit

# Devel - 10.10.10.5
## User

Command 0 - Scan top 200 ports with timing 3 - (Active Scan):
<pre>nmap --top-ports=200 10.10.10.5 -T3</pre>
![command0](https://user-images.githubusercontent.com/26724539/74437641-3c53f080-4e47-11ea-8b70-adc338037c0e.png)
    
Command 1 - Scan using most common scripts - (Service Enum):
<pre>nmap -sC -p 21,80 10.10.10.5</pre>
![command1](https://user-images.githubusercontent.com/26724539/74437642-3cec8700-4e47-11ea-8f98-5de7879d6109.png)    

As observed, the server is running FTP anonymous login and aspnet on the server, so we can upload a .aspx backdoor and exploit it - (Exploitation):

Command 2 - Generating .aspx backdoor:
![command2](https://user-images.githubusercontent.com/26724539/74437645-3d851d80-4e47-11ea-94e8-85b67aae70a0.png)

Command 2.1 - Uploading backdoor:

![command2 1](https://user-images.githubusercontent.com/26724539/74437646-3d851d80-4e47-11ea-84f4-5ab7b66bcf7e.png)

Command 2.2 - Setting exploit, payload configs and start it:
![command2 2](https://user-images.githubusercontent.com/26724539/74437647-3e1db400-4e47-11ea-8525-5d235d9ba8c8.png)     

Command 2.3 - Loading page and exploiting:

![command2 3](https://user-images.githubusercontent.com/26724539/74437649-3eb64a80-4e47-11ea-84ea-e3f239802aa7.png)
![command2 3_p2](https://user-images.githubusercontent.com/26724539/74437651-3eb64a80-4e47-11ea-8580-964eb3c3b923.png)
    
# Root

We can use windows systeminfo and analyse it  - (Post-exploitation):

Command 0 - systeminfo:

![commandr0](https://user-images.githubusercontent.com/26724539/74440806-72946e80-4e4d-11ea-9d27-99ebedf77ada.png)

Based on system version, we found a kernel exploit. We can download and use it.

Link: https://github.com/abatchy17/WindowsExploits/tree/master/MS11-046

Command 1 - uploading and using the exploit:
![commandr1](https://user-images.githubusercontent.com/26724539/74440813-732d0500-4e4d-11ea-8ed8-aa7a0377c9c4.png)

And finally rooted.

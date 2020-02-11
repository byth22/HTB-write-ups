# Legacy - 10.10.10.4

Command 0 - Scan top 200 ports with timing 3 - (Active Scan):
<pre>nmap --top-ports=200 10.10.10.4 -T3</pre>
![img0](https://user-images.githubusercontent.com/26724539/73882789-7dde0d80-4841-11ea-9f00-c06e7f035a8d.png)

Command 1 - Scan to check SMB vulns - (Service Enum):
<pre>nmap -p 139,445,3389 10.10.10.4 --script "smb-vuln*"</pre>
![img1](https://user-images.githubusercontent.com/26724539/73883249-5e93b000-4842-11ea-8f42-2e50f42c1893.png)

Using msfconsole to gain access. Setting payload, exploit and running - (Exploitation):

Command 2 - Setting payload and exploit:
![img2](https://user-images.githubusercontent.com/26724539/73883998-baab0400-4843-11ea-9ffd-9ae096b16019.png)
![img2.1](https://user-images.githubusercontent.com/26724539/74242864-6ed1e200-4cbd-11ea-86fd-5f512c37cfb0.png)

Command 2.1 - Running:
![img2.2](https://user-images.githubusercontent.com/26724539/73884000-bbdc3100-4843-11ea-885c-4e4bc7053638.png)

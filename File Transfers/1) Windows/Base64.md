
This method is pretty simple since all ur really doing is copy and pasting the "file" from one environment to another, though this does only really work for smaller files due to terminal character limitations. Here's how you do it:

### 1 - Taking the file and encoding it in base64
Depending on your host machine (Works both ways, from victim to host or vice versa), you can use:

`PS C:\Users\Username\Desktop> Get-FileHash [The file]`


### 2 - Decode the file

Then you can decode it on the other machine using 

`
`PS C:\Users\Username\Desktop>  [IO.File]::WriteAllBytes("C:\Users\You\output.txt", [Convert]::FromBase64String("Base64 Here"))`

For Windows where:
`[IO.File]::WriteAllBytes(...)` -Writes all the bytes to the file path specified
`[Convert]::FromBase64String("Base64 Here")` - Decodes the Base64 into a byte array


# Note:
if you only have a cmd CLI and not powershell, you can either invoke one using

`C:\Users\You> powershell`

or youcan wrap the powershell command like this

`C:\Users\You> powershell -Command "[IO.File]::WriteAllBytes("C:\Users\You\output.txt", [Convert]::FromBase64String("Base64 Here"))`"`
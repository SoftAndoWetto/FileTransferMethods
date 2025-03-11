using cURL to get files from online is easy, Its only:

`curl -o <PATH> <URL with Data>`

`-o` - Output

And that's it.
The only thing probably to note is that, if its from an ftp server for example, its just
`curl -o ftp://<IP Address>`

You can also, rather than saving the file, pipe it directly to run with this

`curl <PATH> | bash`
Wherte it just takes whats at the path and runs it as code. Obviously thought, the website hosting the information must be ONLY code. The example used for this was
https://raw.githubusercontent.com/rebootuser/LinEnum/master/LinEnum.sh
Which hosts the raw code on a webpage for LinEnum script
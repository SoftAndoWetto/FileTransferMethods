
This method is pretty simple since all ur really doing is copy and pasting the "file" from one environment to another, though this does only really work for smaller files due to terminal character limitations. Here's how you do it:

### 1 - Taking the file and encoding it in base64
Depending on your host machine (Works both ways, from victim to host or vice versa), you can use:

`> cat [The File] | base64`
(Just so this is as beginner as friendly as possible "|" this is called a pipe, and is used to take the results from 1 command and put it straight into another. And cat, just reads the contents of the file)
``

### 2 - Decode the file

Then you can decode it on the other machine using 

`echo -n 'The Base64 in here' | base64 -d > output.txt`

Where:
`-n` just puts it all in 1 line 
`-d` is for decoding the base64
`> output.txt` This takes the output and writes it to the file names "output.txt"`
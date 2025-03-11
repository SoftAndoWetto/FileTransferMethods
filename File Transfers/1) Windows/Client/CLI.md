# Curl
I actually didnt know, but Windows 10+ comes with curl so you can use

`curl -O <File Name> <URL>`
To download a file from online, where:

`-O` - Is output

# Bitsadmin

You can also use Bitsadmin (Background Intelligence Transfer Service) to download files, one benefit of this is that it uses idle bandwidth, meaning it will remain more lowkey sine it uses what it can get, rather than hogging it all, but this can also mean it might take longer but its not like ur downloading warzone or something huge.

`bitsadmin /transfer NameOfJob /download <URL> <Destination>`
Where:

`/Transfer` - Specifies that this is a transfer
`NameOfJob` - This is the name you give the download job, you can name this something that may blend in more as a background process to further reduce suspicion


# Writing

There is a
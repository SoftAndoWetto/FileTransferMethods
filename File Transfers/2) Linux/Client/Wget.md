Similarly to [[cURL]] this is also very simple

`
`wget <URL> -O <Output Path>`
`
`-O` - 

If you would like to pipe the output directly to run instead of saving it locally for forensic reasons you can also use:

`wget <URL> -qO- | <Whatever it uses to run>`

`-q` - Quiet mode
`-O-` - which is stdout (standard output) which is what lets it be piped
`<Whatever it uses to run>` - This just means whether its like, bash or python, or any other language
# HTTPServer

#### Ben Smith

#### Usage
Compile with `make`.
Execute with `./web_server <port-number> <root-directory>` where '\<port-number\>'
is the port you wish to connect with and '\<root-directory\>' is highest level
directory containing files that can be served.

#### Description
This HTTP server continuously receives and responds to http GET requests.
Requests can be a maximum size of 8 KB long. Only GET methods are handled, all
other methods will result in a '405 Method Not Allowed' response. If the request
is a GET method then the URI will be parsed out. URIs can be a maximum of 2000
characters. If the URI is a directory ('/root/html/') then the server will try
to serve 'index.html' in the given directory ('/root/html/index.html'). If a URI
includes either '~' or '..' the resource will not be served to prevent access of
files outside of the root directory. Otherwise the resource will be served if it
exists.

GitHub URL: https://github.com/ben0815/HTTPServer

# Developing a Simple Webserver
## AIM:

To develop a simple webserver to serve html pages.
## DESIGN STEPS:
### Step 1:

HTML content creation
### Step 2:

Design of webserver workflow
### Step 3:

Implementation using Python code
### Step 4:

Serving the HTML pages.
### Step 5:

Testing the webserver
## PROGRAM:

from http.server import HTTPServer, 

BaseHTTPRequestHandler
content =
 """
<!DOCTYPE html>
<html>
<head>
<title>My webserver</title>
</head>
<body>
<h1>Name:A.Ruchitha Reddy</h1>
<h2>21005032</h2>
<h2>Artificial inteligence And Data science</h2>
</body>
</html>
"""
class myhandler(BaseHTTPRequestHandler):

def do_GET(self):

print("request received")

self.send_response(200)

self.send_header('content-type', 'text/html; 
charset=utf-8')

self.end_headers()

self.wfile.write(content.encode())

server_address = ('',8080)

httpd = HTTPServer(server_address,myhandler)

print("my webserver is running...")


## OUTPUT:
![output](https://github.com/RuchithaReddy28/Web_server/blob/main/simple%20web%20server.PNG?raw=true)

## RESULT:
The program is Executed
# EX01 Developing a Simple Webserver
## Date:

## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:
from http.server import HTTPServer,BaseHTTPRequestHandler

content='''
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
<html>
<head>
<title>Software Companies</title>
</head>
<body bgcolor="white">
<h1 style="font-family:'Courier New', Courier, monospace ; font-size: 50px;"align="center">Top Software Companies</h1>
<table border="5" bordercolor='black' cellspacing="4" cellpadding="6" height="30" width="50"align="center">
<caption style="font-family:'Courier New', Courier, monospace ;font-size: 15px;"align="center"><b>Top Five Revenue Generating Software Companies</b></caption><br>
<tr><br>
<th>Rank</th>
<th>Company</th>
<th>Revenue</th>
</tr>
<tr>
<td align="center">1</td>
<td align="center">Alphabet</td>
<td align="center">$282B</td>
</tr>
<tr>
<td align="center">2</td>
<td align="center">Microsoft</td>
<td align="center">$211B</td>
</tr>
<tr>
<td align="center">3</td>
<td align="center">Amazon</td>
<td align="center">$478B</td>
</tr>
<tr>
<td align="center">4</td>
<td align="center">IBM</td>
<td align="center">$60B</td>
</tr>
<tr>
<td align="center">5</td>
<td align="center">Oracle</td>
<td align="center">$49B</td>
</tr>
</body>
</html>
</body>
</html>

'''

class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200) 
        self.send_header("content-type", "text/html")       
        self.end_headers()
        self.wfile.write(content.encode())

print("This is my webserver") 
server_address =('',8000)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()
class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200) 
        self.send_header("content-type", "text/html")       
        self.end_headers()
        self.wfile.write(content.encode())

print("This is my webserver") 
server_address =('',8000)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()


## OUTPUT:
![image](https://github.com/JAYASREE24032006/simplewebserver/assets/144360800/dfeb6a50-f1c4-46ae-89f0-234dcca9c33d)



## RESULT:
The program for implementing simple webserver is executed successfully.

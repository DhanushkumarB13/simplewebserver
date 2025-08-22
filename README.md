# EX01 Developing a Simple Webserver
## Date: 22/08/2025
## NAME: B. DHANUSH KUMAR
## REG NO: 212224240034

## AIM:
To develop a simple webserver to serve html pages and display the list of protocols in TCP/IP Protocol Suite.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Import the necessary modules.

### Step 5:
Define a custom request handler.

### Step 6:
Start an HTTP server on a specific port.

### Step 7:
Run the Python script to serve web pages.

### Step 8:
Serve the HTML pages.

### Step 9:
Start the server script and check for errors.

### Step 10:
Open a browser and navigate to http://127.0.0.1:8000 (or the assigned port).

## PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<html>
<head>
<title>Top 5 Software Companies in Revenue</title>
</head>
<body>
<h1 align="center">Top Five Software Companies in Revenue </h1>
<table align="center" width="540" cellspacing="2" cellpoding="4" border="2">
<tr align="center">
        <th bgcolor="aquablue">S.NO</th>
        <th bgcolor="aquablue">NAME OF THE COMPANY</th>
        <th bgcolor="aquablue">REVENUE</th>
        <th bgcolor="aquablue">GROWTH RATE</th>
        </tr>
        <tr align="center">
        <td>1</td>
        <td>Microsoft</td>
        <td>$32.2B</td>
        <td>39%</td>
        </tr>
        <tr align="center">
        <td>2</td>
        <td>Amazon</td>
        <td>$35.03B</td>
        <td>37%</td>
        </tr>
        <tr align="center">
        <td>3</td>
        <td>IBM</td>
        <td>$35.03B</td>
        <td>14%</td>
        </tr>
        <tr align="center">
        <td>4</td>
        <td>Salesforce</td>
        <td>$17.1B</td>
        <td>25%</td>
        <tr align="center">
        <td>5</td>
        <td>Goole</td>
        <td>$8.92B</td>
        <td>53%</td>
        </tr>
        </body>
        </html>
"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8000)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
```

## OUTPUT:

<img width="1032" height="539" alt="Screenshot 2025-08-22 132039" src="https://github.com/user-attachments/assets/fc357066-affd-46e8-9537-a4387f182980" /> 

<img width="1041" height="615" alt="Screenshot 2025-08-22 132101" src="https://github.com/user-attachments/assets/04f6fec9-f795-44c7-9137-8d555dcf17e5" />



## RESULT:
The program for implementing simple webserver is executed successfully.

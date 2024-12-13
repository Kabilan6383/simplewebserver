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
```
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<!DOCTYPE html>
<html>
<head>
<title>TOP SOFTWARE COMPANIES IN REVENUE</title>
</head>
<body>
<center><h1> TOP SOFTWARE COMPANIES IN REVENUE</h1></centre>
<table border="10" cellspacing="10"  width="75" height="100"
            <tr align="center">
                <th bgcolor="yellow">Rank</th>
                <th bgcolor="yellow">Company</th>
                <th bgcolor="yellow">Sales</th>
                <th bgcolor="yellow">Nationality</th>
            </tr>
            <tr align="center">
                <td bgcolor="blue">1</td>
                <td bgcolor="red">Microsoft</td>
                <td bgcolor="red">57.9</td>
                <td bgcolor="red">USA</td>
            </tr>
            <tr align="center">
                <td bgcolor="blue">2</td>
                <td bgcolor="red">Oracle</td>
                <td bgcolor="red">21.0</td>
                <td bgcolor="red">USA</td>
            </tr>
            <tr align="center">
                <td bgcolor="blue">3</td>
                <td bgcolor="red">SAP</td>
                <td bgcolor="red">16.1</td>
                <td bgcolor="red">Germany</td>
            </tr>
            <tr align="center">
                <td bgcolor="blue">4</td>
                <td bgcolor="red">Computer Associates</td>
                <td bgcolor="red">4.2</td>
                <td bgcolor="red">USA</td>
            </tr>
            <tr align="center">
                <td bgcolor="blue">5</td>
                <td bgcolor="red">Adobe</td>
                <td bgcolor="red">3.4</td>
                <td bgcolor="red">USA</td>
            </tr>
 </table>       
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
![Screenshot 2024-12-13 190947](https://github.com/user-attachments/assets/b66dd822-1fd7-4238-9dcf-c5037d8a2084)
![Screenshot 2024-12-13 190849](https://github.com/user-attachments/assets/cfe48d30-b1da-4675-834f-b1b6d1b6b3c5)




## RESULT:
The program for implementing simple webserver is executed successfully.

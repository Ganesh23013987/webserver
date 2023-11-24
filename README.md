# Developing a Simple Webserver

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

HTML content creation is done

### Step 2:

Design of webserver workflow

### Step 3:

Implementation using Python code

### Step 4:

Serving the HTML pages.

### Step 5:

Testing the webserver

## PROGRAM:
```from http.server import HTTPServer,BaseHTTPRequestHandler

content='''
<!doctype html>
<html>
<head>
<title> My Web Server</title>
</head>
<body>
<h1>Top Five Web Application Development Frameworks</h1>
<h2>1.Django</h2>
<h2>2. MEAN Stack</h2>
<h2>3. React </h2>
<h2>4.spring</h2>
<h2>5.Angular</h2>
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
server_address =('',80)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()```

## OUTPUT:
### server output:
<img width="602" alt="Server output" src="https://github.com/Ganesh23013987/webserver/assets/147473768/fe3c8f1d-8d8c-47d7-9638-8f38e09da963">
### client output:
<img width="592" alt="client output" src="https://github.com/Ganesh23013987/webserver/assets/147473768/6e32b47e-7744-4c68-b21b-89c3fce8422c">

## RESULT:
The program is executed succesfully.

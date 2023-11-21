# Developing a Simple Webserver
Name : KAMALESH R
REFERENCE NO : 23001711

# AIM:

Develop a webserver to display about top five web application development frameworks.

# DESIGN STEPS:

## Step 1:

HTML content creation is done

## Step 2:

Design of webserver workflow

## Step 3:

Implementation using Python code

## Step 4:

Serving the HTML pages.

## Step 5:

Testing the webserver

# PROGRAM:
Type your code here
```python
from http.server import HTTPServer, BaseHTTPRequestHandler

content = """
<html>
<head>
</head>
<body>
<h1>Welcome</h1>
</body>
</html>
"""

class HelloHandler (BaseHTTPRequestHandler):
    def do_GET (self):
        self.send_response(200)
        self.send_header('Content-type', 'text/html; charset=utf-8')
        self.end_headers ()
        self.wfile.write(content.encode())

server_address = ('', 80)
httpd = HTTPServer (server_address, HelloHandler)
httpd.serve_forever()
```
# OUTPUT
![Screenshot 2023-11-21 093459](https://github.com/KAMALESHNITHYA/Web_server/assets/145743119/0f07d985-dd6c-41cd-ad82-078c4e34a87d)


# RESULT:

The program is executed succesfully

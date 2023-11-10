# Developing a Simple Webserver
Name: Kumarteja naramala
Dept:AI&DS
ID: 23003525
email : tejakumar751@gmail.com

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
```from http.server import HTTPServer , BaseHTTPRequestHandler

content="""
<html>
<head>
</head>
<body>
<h1>welcome</h1>
</body>
</html>
"""

class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request recieved")
        self.send_response(200)
        self.send_header('Content-type','text/html;charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())

print("This is my webserver")
server_address = ('',80)
httpd = HTTPServer(server_address,HelloHandler)
httpd.serve.forever()
```
# OUTPUT:
![output](https://github.com/KumarTeja751/Web_server/assets/144947756/3fad55a9-c2f3-4274-8850-e9faf54523c2)

# RESULT:

The program is executed succesfully

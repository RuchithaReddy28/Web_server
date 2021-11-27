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
## PROGRAM:<!DOCTYPE html>
<html>

   <head>
      <title>TIME TABLE</title>
   </head>

   <body>
     <h1>Name :A.Ruchitha Reddy<h1></h1>
     <br>Reference no: 21500178<br>
     Department:Artificial Intelligence and DataScience</h1>
      <table border = "1" cellspacing="1" bordercolor="blue" bgcolor="grey">
         <tr>
            <th colspan="8">TIME TABLE</th>
         </tr>
       
         <tr>
            <th>DAYS</th>
            <th>1</th>
            <th>2</th>
            <th>3</th>
             <th>4</th>
             <th>-</th>
            <th>5</th>
            <th>6</th>
           
         </tr>
       
 
  <tr>
             <td>Monday</td>
             <td>Fundamentals of Web Technology/Karthi Govindharaju/19AI401</td>
             <td>Fundamentals of Web technology/Karthi Govindharaju/19AI401</td>
             <td>Linear Algebra Laboratory/Jaba Jasphin/19MA221</td></td>
             <td>Linear Algebra Laboratory/Jaba Jasphin/19MA221</td>
           <td>lunch break</td>
             <td>Mathamatics for Artificial Intelligence/Jaba Jasphin/19MA220</td>
             <td>Mathamatics for Artificial Intelligence/Jaba Jasphin/19MA220</td>
</tr>
<tr>
             <td>Tuesday</td>
             <td>Soft Skills/Praveen P/19EY701</td>
             <td>Soft Skills/Praveen P/19EY701</td>
             <td>Engineering Design and Modeling/Sellakumar S/19AI302</td>
             <td>Engineering Design and Modeling/Sellakumar S/19AI302</td>
             <td>Engineering Mechanics and Product Development/Sellakumar S/19AI303</td>
             <td>Engineering Mechanics and Product Development/Sellakumar S/19AI303</td>
             
             
</tr>
<tr>
             <td>Wednesday</td>
             <td>Free Period</td>
             <td>Free Period</td>  
             <td>Mathematics for Artificial Intelligence/Jaba Jasphin/19MA220 </td>
             <td>Mathematics for Aritificial Intelligence/Jaba Jasphin/19MA220</td>
             <td>lunch break</td>
             <td>Fundamentals of Web Technology/Karthi Govindharaju/19AI401</td>
             <td>Fundamentals of Web Technology/Karthi Govindharaju/19AI401</td>
</tr>
  <tr>
             <td>Thursday</td>
             <td>Engineering Mechanics and Product Development/Sellakumar S/19AI303</td>
             <td>Engineering Mechanics and Product Development/Sellakumar S/19AI303</td>
             <td>Python Programming/Jaba Jasphin/19AI301 </td>
             <td>Python Programming/Jaba Jasphin/19AI301</td>
             <td>Mentoring -AD1/Karthik S/ECA051-AD</td></TD>
             <td>lunch break</td>
             <td>Engineering Design and Modeling/Sellakumar S/19AI302</td>
             <td> Engineering Design and Modeling/Sellakumar S/19AI302</td>
</tr>
<tr>
             <td>Friday</td>
             <td>Environmental Science/19MC802</td>
             <td>Environmental Science/19MC802</td>
             <td>Python Programming/Jaba Jasphin/19AI301</td>
             <td>Python Programming/Jaba Jasphin/19AI301</td>
              <td>lunch break</td>
             <td>Web Technology Laboratory/Karthi Govindharaju/19AI402</td>
             <td>Web Technology Laboratory/Karthi Govindharaju/19AI402</td>
</tr>
 
       
      </table>
     
   </body>
</html>



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
The program is Exeuted
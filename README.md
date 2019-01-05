# Vulners-Scanner

Vulnerability scanner based on vulners.com audit API https://vulners.com  
This is a modified version of vulners-scanner which can generate vulners scan output in csv format.  
All credits goes to vulners.com  

# How to use?  
Clone the repository  
```
$ git clone https://github.com/le0li9ht/Vulners-Scanner
```
Go to cloned directory  
```
$cd Vulners-Scanner
```
Add execution permissions for the script  
```
$ chmod +x vulners-scanner.py
```
Run the scan  
``` 
$ ./vulners-scanner.py >scan.csv
```
For generating a nice tabular report from the vulners csv file please clone the nmaptable
```
$ git clone https://github.com/jgamblin/nmaptable
```
Move the scan.csv file(vulners report) to the nmaptable directory and change its name to data.csv
```
$ rm nmaptable/data.csv
$ mv scan.csv nmaptable/data.csv
```
Run the http-server(nodejs http server)
```
$ http-server
```
Use the wkhtmltopdf for converting the html to nice tabular form of output.
```
wkhtmltopdf --viewport-size 1024x768 -O Landscape http://127.0.0.1:8080/nmaptable/nmap.html vulners-report.pdf
  
```
Example report generated through above steps  
![](https://raw.githubusercontent.com/le0li9ht/Vulners-Scanner/master/Vulners-Report.png)




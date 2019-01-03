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
For a redable vulners report use the https://github.com/jgamblin/nmaptable and provide the scan.csv file as input to it to get a
readable report as shown below





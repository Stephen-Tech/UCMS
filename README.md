# UCMS
## Vulnerability Name:
UCMS has cross site scripting attack (XSS) in the title bar of all systems.
## Vulnerability version number: 
UCMS v1.4.6
## Vulnerability:
high risk
## Vulnerability Description:
Without checking the data contained in the dynamic content, it is transmitted to the Web user. Malicious content delivered to a Web browser usually takes the form of a JavaScript snippet, but may also contain some HTML, Flash, or any other code that can be executed by the browser, such as private data (such as cookies or other session information) that is transmitted to an attacker. Under the control of the attacker, guide the victim into malicious network content; or use vulnerable sites for other malicious operations on the user's machine.
## Loophole URL:
http://demo.uuu.la/ucms/?do=list&cid=5    
http://demo.uuu.la/ucms/?do=list&cid=6
## Vulnerability Description:
http://demo.uuu.la/ucms/?do=list&cid=5  
We edit the title of the category after testing the account into the background.
![image](https://github.com/Stephen-Tech/UCMS/blob/master/1.png)   
Modified to XSS code
![image](https://github.com/Stephen-Tech/UCMS/blob/master/2.png)  
Click "Edit" and then play the box.
![image](https://github.com/Stephen-Tech/UCMS/blob/master/3.png)  
Enter the column of the article to edit the title.
![image](https://github.com/Stephen-Tech/UCMS/blob/master/4.png)
![image](https://github.com/Stephen-Tech/UCMS/blob/master/5.png)  
Click "Edit" and click "Browse".
![image](https://github.com/Stephen-Tech/UCMS/blob/master/6.png)  
XSS frame appears.
![image](https://github.com/Stephen-Tech/UCMS/blob/master/7.png)
![image](https://github.com/Stephen-Tech/UCMS/blob/master/8.png)
Malicious code can be executed through XSS. 
## Suggestions for rectification:
Delete and strengthen the input validation mechanism to filter dangerous characters such as < >, > &amp; amp; and so on.

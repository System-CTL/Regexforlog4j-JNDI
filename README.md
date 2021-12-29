# Regexforlog4j-JNDI
Log4Shell is the name given to a vulnerability affecting Log4Shell (CVE-2021-44228). The vulnerability is associated with the Log4j JNDI lookup feature, which on versions <= 2.17.1, by default creates objects of the class returned by the lookup operation. 

SOC guys working day and night for protecting the organization but sometimes we don't have the mechanism for protecing against particular threat like in some moment of life we were helpless but After the Storm the Sun Will Shine Again.
Yup log4j, being a SOC analyst my core skill not comprises on writting regex but have some hands-on knowledge about it. If we talk about current scenerio, the vulnerability exploited massively and attempts are made in each day and good news is the infosec people wrtting long long regex for SIEM solutions and dumb guy be like how you did that but long is not always right ooh sorry, Means optimal solution could be achieved in matter of few lines.I have came to know that everyone is so supportive in cyber community, so hats off to everyone for doing their best for coummunity.    

# For SIEM
- Right now, tested on IBM Qradar.

# Use Case
- Early Detection is the key, Work had been done for detection on payload.
- Likewise, search this regex against every UTF(payload). 
- This is just for detection, Yup i have idea about TTP's.

# My Approach (1.1) - New  
	[^$][jndi]{4}?(:|\/)|[^$][dns]{3}?(:|\/)|[^$][ldap]{4}?(:)|[dns]{3}?(%)|[A-Za-z0-9+\/=]{80}|[^${$]?[{:-]{2}?(j|n|d|i)|[rmiRMI]{3}?(:|\/)|[^$][IIOPiiop]{4}?(:|\/)|[^$][jnd]{3}?(:|\/|%)|[a-zA-Z0-9+\/=]?(base64|Base64)|[^${$]?[{:-]{1}?(j|n|d|i|7|b|p|1)|(0x)?[0-9%a-f]{20}
![image](https://user-images.githubusercontent.com/70237548/147309743-14ac1511-bd62-42d2-b59c-3e17e01141f5.png)

# My Approach (1.0)  
	[^$][jndi]{4}?(:)|[^$][dns]{3}?(:|\/)|[^$][ldap]{4}?(:)|[dns]{3}?(%)|[A-Za-z0-9+\/=]{80}|[^${$]?[{:-]{2}?(j|n|d|i)|[rmiRMI]{3}?(:|\/)|[^$][IIOPiiop]{4}?(:|\/)
 
# Screenshot
![image](https://user-images.githubusercontent.com/70237548/147303519-86aa8beb-9055-42b5-9a54-4679438b7871.png)

# Difficult to detect!
![image](https://user-images.githubusercontent.com/70237548/147303622-d107bfb8-5d85-44c1-8140-6b3eb0ee1f77.png)

# You Can
- kindly let me know if anything wrong in my approach and you can ping me on linkedin.

# Regexforlog4j-JNDI
SOC analyst work day and night for protecting the organization but sometimes we don't have the mechanism for protecing against particular threat like in life in some moment we were helpless but sun shine after storm. Yup log4j, i'm not a pro in wrtting regex but have some hands-on knowledge. For now, i have seen people wrtting long regex for SIEM solution and dumb guy like thinking how you did that but long is not always right ooh sorry, Means optimal solution could be achieved in matter of few words.  

# My Approach 
	[^$][jndi]{4}?(:)|[^$][dns]{3}?(:|\/)|[^$][ldap]{4}?(:)|[dns]{3}?(%)|[A-Za-z0-9+\/=]{80}|[^${$]?[{:-]{2}?(j|n|d|i)|[rmiRMI]{3}?(:|\/)|[^$][IIOPiiop]{4}?(:|\/)

# For SIEM
- Right now, tested on IBM Qradar.

# Use Case
- Early Detection is the key, Work had been done for detection on payload.
- Likewise, search this regex against every UTF(payload). 
- This is just for detection, Yup i have idea about TTP's.
 
# Screenshot
![image](https://user-images.githubusercontent.com/70237548/147303519-86aa8beb-9055-42b5-9a54-4679438b7871.png)

# Difficult to detect!
![image](https://user-images.githubusercontent.com/70237548/147303622-d107bfb8-5d85-44c1-8140-6b3eb0ee1f77.png)



# You Can
- kindly let me know if anything wrong in my approach and you can ping me on linkedin.

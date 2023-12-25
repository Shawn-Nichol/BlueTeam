# Question 1
Use grep to filter result for login filter through the log result to find the page, it should be pretty clear.
```
cat access.log | grep -i "login" 
```
wp-login.php?itsec-hb-token=adminlogin

# Question 2


# Question 3
Google CVE contact-form-7
CVE-2020-35489

# Question 4



# Question 5
Search with
```
cat access.log | grep ".php"
```

![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/61bcfb96-8977-49d1-b1f0-869131d435bd)

fr34k.php
# Question 6
We can filter results by the plugin, that was discovered in the last question. 
```
cat access.log -n | grep -i "fr34k.php"
```
You can identify the last result by using the last line of the query. 
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/b2f3fd7b-332c-4636-af4d-97f31da3df49)


404

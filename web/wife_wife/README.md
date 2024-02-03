For this web challenge solution, we have to use __proto__ to pass the "isAdmin" value to true to the registration.

You can learn more about __proto__ JavaScript function here (Use Google Translate for English Language):
https://www.leavesongs.com/PENETRATION/javascript-prototype-pollution-attack.html

I also had screenshots of some processes of how to get it to work. Basically you need to use BurpSuite and get access to the 
challenge website by intercepting it. Then, send it to the request and modify with the following payload:

Ex:
{"username":"h","password":"h","__proto__":{"isAdmin":true},"inviteCode":"h"}

And click send, check response. If successful, you just need to login with the username and password. 
It will show the flag at the homepage.

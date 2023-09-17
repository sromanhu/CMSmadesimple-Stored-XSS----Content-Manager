# CMSmadesimple Stored XSS v2.2.18

## Author: (Sergio)

**Description:** Cross Site Scripting vulnerability in CMSmadesimple v.2.2.18 allows a local attacker to execute arbitrary code via a crafted script to the Global Meatadata in the Settings- Global Settings Menu.

**Attack Vectors:** Scripting A vulnerability in the sanitization of the entry in the Global Meatadata of "Settings- Global Settings Menu" allows injecting JavaScript code that will be executed when the user accesses the web page.

---

### POC:


When logging into the panel, we will go to the "Settings- Global Settings Menu." section off General Menu.

![XSS Global Metadata](https://github.com/sromanhu/CMSmadesimple-Stored-XSS---Global-Settings/assets/87250597/243e7d1f-2bca-4acc-994a-63f926403700)



We edit that Global Settings Menu that we have created and see that we can inject arbitrary Javascript code in the Global Meatadata field.


### XSS Payload:

```js
<img src=1 onerror=alert("1")
```


In the following image you can see the embedded code that executes the payload in the main web.
![XSS Global Metadata resultado](https://github.com/sromanhu/CMSmadesimple-Stored-XSS---Global-Settings/assets/87250597/ca7fd137-6975-4826-b1be-8dce3970ebee)



</br>

### Additional Information:
http://cszcms.com](http://www.cmsmadesimple.org/

https://owasp.org/Top10/es/A03_2021-Injection/

https://owasp.org/www-community/attacks/xss/

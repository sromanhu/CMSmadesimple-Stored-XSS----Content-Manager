# CMSmadesimple Stored XSS v2.2.18

## Author: (Sergio)

**Description:** Multiple cross-site scripting (XSS) vulnerabilites in CMSmadesimple v.2.2.18 allows a local attacker to execute arbitrary code via a crafted script to the Page Specific Metadata and Smarty data in the Content Manager Menu.

**Attack Vectors:** Scripting A vulnerability in the sanitization of the entry in the "Content Manager Menu" allows injecting JavaScript code that will be executed when the user accesses the web page.

---

### POC:


When logging into the panel, we will go to the "Content- Content Manager Menu." section off General Menu.

![XSS Payload](https://github.com/sromanhu/CMSmadesimple-Stored-XSS----Content-Manager/assets/87250597/96847290-5472-4850-b627-ed23462522db)




We edit that Content Manager Menu that we have created and see that we can inject arbitrary Javascript code in the Page Specific Metadata and Smarty data


### XSS Payload:

```js
<object data=javascript&colon;\u0061&#x6C;&#101%72t('Metadata')>
```

```js
<object data=javascript&colon;\u0061&#x6C;&#101%72t('Smarty')>
```

In the following image you can see the embedded code that executes the payload in the main web.
![XSS Resultado 1](https://github.com/sromanhu/CMSmadesimple-Stored-XSS----Content-Manager/assets/87250597/aacd52d6-3f8c-4c7a-8440-8212a3f680b8)


![XSS Resultado](https://github.com/sromanhu/CMSmadesimple-Stored-XSS----Content-Manager/assets/87250597/2c8b6120-3d6b-4847-8c1a-ce73686601d1)



</br>

### Additional Information:
http://www.cmsmadesimple.org/

https://owasp.org/Top10/es/A03_2021-Injection/

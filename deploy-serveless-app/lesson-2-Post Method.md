## Toubleshooting (@Executioner on slack)
### Steps to resolve error in lesson 2 - POST Method:
``` js 
npm ERR! code ERR_TLS_CERT_ALTNAME_INVALID 
```
---
<p>After getting the above error, I carried out the following steps:</p>

<ol>
  <li>Remove node_modules folder if it exits
    <ol>

 ```bash
rm -rf node_modules
 ```

   </ol>
  </li>
  <li>Remove the package-lock.json file
    <ol>

 ```bash
rm package-lock.json
 ```

   </ol>
  </li>
  <li>Clear npm cache
    <ol>

 ```js
npm cache clean --force
 ```

   </ol>
  </li>
  <li>Install dependencies
    <ol>

 ``` js
 npm install
 ```

   </ol>
  </li>
</ol>

## Toubleshooting
### Steps to resolve 
``` js 
npm ERR! code ERR_TLS_CERT_ALTNAME_INVALID 
```
---
<p>After getting the above error, I carried out the following steps:</p>

<p>1: Remove node_modules folder if it exits</p>

``` js
npm run dev
```

<p>2: Remove the package-lock.json file</p>
```bash
rm package-lock.json
```

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
  <li>In the package.json file, on line 18, replace typescript version
    <ol>

 ``` diff
 - "typescript": "3.4.3"
 + "typescript": "^4.8.3" 
 ```

   </ol>
  </li>


  
</ol>
- rm -rf node_modules
- rm package-lock.json
- npm cache clean --force
- 
npm install typescript@^4.8.3
go to client/src/components/CreateGroups.tsx, on line 49, update catch (e) to catch (e: any)
go to client/src/components/GroupsList.tsx, on line 31, update catch (e) to catch (e: any)
npm install --force


```bash
rm -rf node_modules
```
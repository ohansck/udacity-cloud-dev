## Toubleshooting (@Executioner on slack channel ALX-C2-En)
### Steps to resolve error in lesson 2 - Sending Requests with <code>client</code>:
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
  <li>In the package.json file, on line 18, replace typescript version
    <ol>

 ``` diff
 - "typescript": "3.4.3"
 + "typescript": "^4.8.3" 
 ```

   </ol>
  </li>
  <li>In <code>client/src/components/CreateGroups.tsx</code>, on line 49, update <code>catch (e)</code> block
    <ol>

 ``` diff
 - } catch (e) {
 + } catch (e: any) { 
 ```

   </ol>
  </li>
  <li>In <code>client/src/components/GroupsList.tsx</code>, on line 31, update <code>catch (e)</code> block
    <ol>

 ``` diff
 - } catch (e) {
 + } catch (e: any) { 
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
  <li>Insert your apiEndpoint in <code>client/src/config.ts</code>

 ``` ts
 export const apiEndpoint = 'insertHere' 
 ```

   </ol>
  </li>
  <li>Run the start script

 ``` js
 npm run start 
 ```

   </ol>
  </li>


  
</ol>

---

[Follow me](https://github.com/ohansck) on github

[Connect](https://linkedin.com/in/ohaneme-kingsley) with me on LinkedIn

Kindly give this repo a star if you found it's content useful
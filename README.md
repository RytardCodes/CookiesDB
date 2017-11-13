# CookiesDB
A simple sqlite wrapper that helps you use Basic sql Commands/Codes

## Requirements
  - **NodeJS 8+**  
  - **Any Javascript Code that you want to Use databases on!**
  - **Sqlite3 Installed, please do `npm i --s sqlite3` to install!**
  
## Examples

**updateCookies**:
```js
const cookies = require('cookiesdb');

cookies.updateCookies('userID', 500).then(i => { // Adds 500 to an assigned User ID
  console.log(i) // { ID: 'user', value: 500, text: '' }
  console.log(i.value) // Returns 500
});

/*
  We can also make it remove an amount!
  */
  
  cookies.updateCookies('userID', -500).then(i => { // Removes 500 to an assigned User ID
  console.log(i) // { ID: 'user', value: -500, text: '' }
  console.log(i.value) // Returns -500
});
```  

**fetchCookies**:
```js
const cookies = require('cookiesdb');

cookies.fetchCookies('userID').then(i => { // Fetches values from ID user, then forwards it to i
  console.log(i) // { ID: 'user', value: 0, text: '' }
  console.log(i.value) // Returns 0
});
```

**updateText**:
```js
const cookies = require('cookiesdb');

cookies.updateText('user', 'This is a stored string!').then(i => { // Fetches values from ID user, updates text
    console.log(i) // { ID: 'user', value: 0, text: 'This is a stored string!' }
    console.log(i.text) // 'This is a stored string!'
});
```

## Deprecated Functions:
**fetchValue**

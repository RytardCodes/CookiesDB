# CookiesDB
A simple sqlite wrapper that helps you use Basic sql Commands/Codes

## Requirements
  - **NodeJS 8+**  
  - **Any Javascript Code that you want to Use databases on!**
  
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

**getValue**:  
```js  
const cookies = require('cookiesdb');  
var my_obj = {
  user: 'Rytard',
  age: '19'
};

cookies.getObject(my_obj).then(c => { // Gets the Defined Object
  console.log(c) // { user: 'Rytard', age: '19' }
  console.log(c.user) // 'Rytard'
  console.log(c.age) // '19'
});  
```

## Updates
  - **Added `getObject` Function**

## Projects that Use CookiesDB
[**Megaphone**](https://github.com/RytardCodes/Megaphone)  

## Join our Chat!
Link: [Here!](https://discord.gg/d34Cs4)

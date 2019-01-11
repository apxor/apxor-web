# Apxor Web SDK
      
#### Install through NPM

```
npm i -s apxor
```

#### Import and initialize SDK in root of your application

```javascript
import Apxor from 'apxor'; //ES6
//var Apxor = require('apxor'); //ES5

Apxor.init('YOUR_SITE_ID', {
    debug: true //remove this option in production
});

```

#### APIs:

```javascript
import Apxor from 'apxor';
```

##### UserId
```javascript
Apxor.setUserId(String);
```
    
> Eg:
```javascript
Apxor.setUserId("user@example.com");
```
    
***

##### PageView:
```javascript
Apxor.logPageView(location.pathname); //String URL pathname
```

> Eg:
```javascript
Apxor.logPageView("/about.html");
```
    
***
    
##### Events:
```javascript
Apxor.logEvent(name, properties, [category]); //All Strings
```
    
> Eg:
```javascript
Apxor.logEvent("ADD_TO_CART", {
    "userId": "user@example.com",
    "value": "1299",
    "item": "Sony Head Phone 1201" 
}, "PRODUCT_PURCHASE");
```
    
***
    
##### User Properties:
```javascript
Apxor.setUserProperties({
    "property1": "value",
    "property2": "value2"
});
```
    
> Eg:
```javascript
Apxor.setUserProperties({
    "gender": "male",
    "age": "24"
});
```
    
***

##### Session Properties:
```javascript
Apxor.setSessionProperties({
    "property1": "value",
    "property2": "value2"
});
```
    
> Eg:
```javascript
Apxor.setSessionProperties({
    "language": "en",
    "location": "Hyderabad"
});
```

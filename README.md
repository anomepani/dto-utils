# DTO-UTILS Inspired from Dot Net Data Transfer Object Concept, Utility contains method which rename keys in existing object using plain JavaScript code.

# DTO-UTILS - Javascript utility to rename specific keys from array of object or collection easily

### DTO-UTILS currently contains one method `mapTo`

## Installation

In a browser:

Using npm:
```shell
$ npm i -g npm
$ npm i --save dto-utils
```

In Node.js:
```js
// Load dto utils
var DTO = require('dto-utils');
```

How to use:

```js
var collection=[{"category":"version control",url:"https://www.github.com"},{"category":"search engine",url:"https://www.google.com"}];

//Provide key value pair in which key is old key and value is new key(renamed key)
var newKeys={"category":"type"};

var isAllowKeyOverwrite=false;

// By default isAllowKeyOverwrite is true in utils, you can override by pssing appropriate flag
var newCollection=DTO.mapTo(collection,newKeys,isAllowKeyOverwrite); 

// newCollection have updated value like this [{"type":"version control",url:"https://www.github.com"},{"type":"search engine",url:"https://www.google.com"}]

```
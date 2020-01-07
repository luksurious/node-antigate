node-antigate
-------------

antigate.com API client for node.js

Fork of https://github.com/ssbb/node-antigate (previously on Bitbucket)

How to install
--------------

    $ npm install antigate


How to use
----------

```javascript
var Antigate = require('antigate');


var ag = new Antigate('YOUR_ANTIGATE_KEY_HERE');


// Recognize the captcha by URL
ag.processFromURL('CAPTCHA_URL', function(error, text, id) {
  if (error) {
    throw error;
  } else {
    console.log(text);
  }
});

// Recognize the captcha from file
ag.processFromFile('CAPTCHA_FILE_PATH', function(error, text, id) {
  if (error) {
    throw error;
  } else {
    console.log(text);
  }
});

// Recognize the captcha from base64 string
ag.process('BASE_64_STRING', function(error, text, id) {
  if (error) {
    throw error;
  } else {
    console.log(text);
  }
});

// Report bad captcha
ag.report('CAPTCHA_ID_HERE');

// Get you blanace
ag.getBalance(function(error, balance) {
  if (error) {
    throw error;
  } else {
    console.log(balance);
  }
}

```

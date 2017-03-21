# yavjs.js

yavjs is a fork of yavjs.js and is lightweight JavaScript form validation library.

## Features

- Validate form fields from over a dozen rules
- Can call manually field validation and form validation
- No dependencies
- Customizable Messages
- Supply your own validation callbacks for custom rules
- Chainable customization methods for ease of declaration
- Works in all major browsers, (even IE6!)
- Modeled off the CodeIgniter form validation API

## How to use

```javascript
    var validator = new FormValidator('example_form', [{
        name: 'req',
        display: 'required',
        rules: 'required'
    }, {
        name: 'alphanumeric',
        rules: 'alpha_numeric'
    }, {
        name: 'password',
        rules: 'required'
    }, {
        name: 'password_confirm',
        display: 'password confirmation',
        rules: 'required|matches[password]'
    }, {
        name: 'email',
        rules: 'valid_email'
    }, {
        name: 'minlength',
        display: 'min length',
        rules: 'min_length[8]'
    }, {
        names: ['fname', 'lname'],
        rules: 'required|alpha'
    }], function(errors) {
        if (errors.length > 0) {
            // Show the errors
        }
    });
```

## Documentation

You can view everything at https://github.com/pbellerive/yavjs/

## Browserify

It is published to npm under yavjs

```
npm install yavjs
```

[![ghit.me](https://ghit.me/badge.svg?repo=rickharrison/yavjs.js)](https://ghit.me/repo/rickharrison/yavjs.js)

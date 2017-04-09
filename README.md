# yavjs.js

yavjs is a fork of validatejs.js and is lightweight JavaScript form validation library.

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
    To bind on form submit event.
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
    With autload you need to add inline attributes
    data-yavjs-rules = same syntax as in the declaration of the rules
    data-yavjs-display = The display name to use in message else name is used
    data-yavjs-on = a json compose of 2 property : on:eventName, callback
    The callback of data-yavajs-on receive two parameter, the event and errorObject
    
    errorObject =   id: field.id,
                    display: field.display,
                    element: field.element,
                    name: field.name,
                    message: message,
                    messages: [],
                    rule: method
    
## Documentation

You can view everything at https://github.com/pbellerive/yavjs/

## Browserify

It is published to npm under yavjs

```
npm install yavjs
```
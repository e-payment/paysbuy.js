# Paysbuy.js
Client side JavaScript library for tokenizing cards. Currently supports these browsers:

* Chrome - v2 and above
* Firefox - v1 and above
* Internet Explorer - v8 and above
* Safari - v4 and above
* Opera - v9 and above
* Internet Explorer - v6-7 (only in compatibility mode, with Flash installed, and TLS 1.0 enabled)


## Setup

Insert the `paysbuy.js` or minified `paysbuy.min.js` script into your page:

```html
<script src="paysbuy.min.js"></script>
```

Then set your public key somewhere on your page in a `script` tag

```js
Paysbuy.setPublicKey('pub_hrkK7qM6Can2vCsolp');
```

This is all the set up required to start tokenizing cards using the PAYSBUY servers.


## API

### setPublicKey(key)

This sets up your public key to authenticate with the PAYSBUY servers

**Arguments:**

* `key` (required) - the public key that you can find in **where??**

### createToken(object, callback)

This will tokenize a card with the API. This token is used instead of the card number when using the PAYSBUY APIs to make charges etc.

**Arguments:**

* `object` (required) - a javascript object with the card details:  `card_number`, `card_expiry_date` (MM-YYYY format), and `card_cvn` (3 digits).
* `callback`: (required) - a callback that will be triggered when a response is received from PAYSBUY, or the request fails. Two arguments are passed to the callback: the HTTP status (e.g. `200` for success), and the response from the tokenisation API.

### Example

A working example showing how to use this library can be found in [`client_sample.html`](https://github.com/paysbuy/paysbuy.js/blob/master/client_sample.html).

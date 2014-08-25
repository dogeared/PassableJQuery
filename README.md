PassableJQuery
==============

Passable JQuery Plugin

To use, register the input field that will be used for the `secret` and the input field that will be used for the `nickname`.

```
$('input[name="secret"]').passable('register_secret_el');
$('input[name="nickname"]').passable('register_nickname_el');
```

NOTE: registering the secret input field will automatically convert it to a password field with protected input. 
Also, the text entered in the secret field will be saved to local storage when the password is generated.
If the secret is saved in localStorage, the value will automatically be put into the secret input field when it is registerd.

To generate the password, call the `passable` function. 
This should only be done after the `secret` and `nickname` elements have been registered.

```
var password = $.passable();
```

NOTE: There is not error checking of any kind yet. This should not be used under any circumstances in a production environment.

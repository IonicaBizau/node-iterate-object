<!---------------------------------------------------------------------------->
<!-- STOP, LOOK & LISTEN!                                                   -->
<!-- ====================                                                   -->
<!-- Do NOT edit this file directly since it's generated from a template    -->
<!-- file, using https://github.com/IonicaBizau/node-blah                   -->
<!--                                                                        -->
<!-- If you found a typo in documentation, fix it in the source files       -->
<!-- (`lib/*.js`) and make a pull request.                                  -->
<!--                                                                        -->
<!-- If you have any other ideas, open an issue.                            -->
<!--                                                                        -->
<!-- Please consider reading the contribution steps (CONTRIBUTING.md).      -->
<!-- * * * Thanks! * * *                                                    -->
<!---------------------------------------------------------------------------->

# iterate-object [![Donate now][donate-now]][paypal-donations]

A convenient way to iterate objects.

## Installation

```sh
$ npm i iterate-object
```

## Example

```js
// Dependencies
var IterateObject = require("iterate-object");

// Iterate this object
IterateObject({
    name: "Bob"
  , age: 42
}, function (value, name) {
    console.log(name, value);
});
// => "name", "Bob"
//    "age", 42

// Iterate an array
IterateObject([
    1, 2, 3, 4, 5, 6, 7
], function (value, i) {
    console.log("v[" + i + "] = " + value);
});
// => v[0] = 1
//    v[1] = 2
//    v[2] = 3
//    v[3] = 4
//    v[4] = 5
//    v[5] = 6
//    v[6] = 7

// Iterate an array
IterateObject([
    "Alice", "Bob", "Carol", "Dave"
], function (value, i, arr) {
    console.log("Current: " + value + (arr[i + 1] ? " Next:" + arr[i + 1] : ""));
});
// => Current: Alice Next:Bob
//    Current: Bob Next:Carol
//    Current: Carol Next:Dave
//    Current: Dave

```

## Documentation

### `IterateObject(obj, fn)`
Iterates an object. Note the object field order may differ.

#### Params
- **Object** `obj`: The input object.
- **Function** `fn`: A function that will be called with the current value, field name and provided object.

#### Return
- **Function** The `IterateObject` function.

## How to contribute
Have an idea? Found a bug? See [how to contribute][contributing].

## License
[KINDLY][license] © [Ionică Bizău][website]–The [LICENSE](/LICENSE) file contains
a copy of the license.

[license]: http://ionicabizau.github.io/kindly-license/?author=Ionic%C4%83%20Biz%C4%83u%20%3Cbizauionica@gmail.com%3E&year=2015
[contributing]: /CONTRIBUTING.md
[website]: http://ionicabizau.net
[docs]: /DOCUMENTATION.md
[paypal-donations]: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=MG98D7NPFZ3MG
[donate-now]: http://i.imgur.com/jioicaN.png
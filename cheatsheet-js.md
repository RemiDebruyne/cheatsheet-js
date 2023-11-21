# Javascript cheat sheet

## Functions

## Loops
- While
- Do while
- for()

## Objects

- Declare an object :
``` js
let objectName = {
    key: value,
    key: value,
    "multiple words key": value, //key with multiple words have to be declared in strings
    key, // is equal to key : key if the key and value have the same name
    key,
}
```
- `"key" in object` : test if the "key" exists in the object, it returns a boolean value. It allows to test if a key exist even if it is undefined or null
- `object.key` : access the property
- `object["property"]` : access the property from a `variable` 
- Difference between a copy and a clone :
    - copy : references the same data
    ```js
    let user = { name: 'John' };

    let admin = user;

    admin.name = 'Pete'; // changes the the value from the name key to Pete from Jhon

    alert(user.name); // returns Pete and not Jhon because the user key and admin key were referencing the same thing (they both look at the same adress for informations)
    ```
    - clone : the clone has its own references even if they are the same as another object. With the example above, if we cloned admin from user then changed the value of the `name` key, `alert(user.name)`would have returned "Jhon" and not "Pete" since only the admin reference was changed
- `Object.assign(dest, source1, source2)` : clone an object from `sources` to `destination`
- `let cloneName =  structuredClone(object)` : clone most type of data, including arrays and imbriqued date such as an object into an object
- clone loop : serve similair function as `Object.assign`
```js
for (let key in user) {
  clone[key] = user[key];
}
```


## Methods

### String
### Number
### Array
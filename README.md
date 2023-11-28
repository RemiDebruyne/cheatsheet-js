# Javascript cheat sheet

## Loops
- While
- Do while
- for()

## Functions

- Declare a function with parameters, then call the function with `value1` `value2` being the value of the parameters
```js
  function name(parameter1, parameter2,...parameterN){
    //code
    }
  name(value1, value2)
```

- Arrow functions
```js
  let func = (arg1, arg2, ..., argN) => expression;

  let sum = (a, b) => a + b; // example

  let sayHi = () => alert("hello"); // example of a function without arguments

  // example of dynamic function using arrow function
  let age = prompt("What is your age?", 18);

  let welcome = (age < 18) ?
    () => alert("Hello!") :
    () => alert("Greetings!");

  welcome(); // ok now
```

- multiligne arrow function
```js
  let sum = (a, b) => {  // brackets are necessary in multiligne arrow function
    let result = a + b;
    return result; // When using brackets, return is mandatory
  };

  alert( sum(1, 2) ); // 3
```




## Objects
### Declare an object 
- Object property = key + value
- Declare an object :
  ``` js
    let objectName = {
        key: value, // property one
        key: value, //property two
        "multiple words key": value, //key with multiple words have to be declared in strings
        key, // is equal to key : key if the key and value have the same name
        key,
    }
  ```

### Access keys in object
  - `"key" in object` : test if the "key" exists in the object, it returns a boolean value. It allows to test if a key exist even if it is undefined or null
  - `object.key` : access the property
  - `object["property"]` : access the property from a `variable` 

### Cloning and copying objects
  - Difference between a **copy** and a **clone** :
      - **copy** : references the same data

        ```js
          let user = { name: 'John' };

          let admin = user;

          admin.name = 'Pete'; // changes the the value from the name key to Pete from Jhon

          alert(user.name); // returns Pete and not Jhon because the user key and admin key were referencing the same thing (they both look at the same adress for informations)
        ```
      - **clone** : the clone has its own references even if they are the same as another object. With the example above, if we cloned admin from user then changed the value of the `name` key, `alert(user.name)`would have returned "Jhon" and not "Pete" since only the admin reference was changed

  - `Object.assign(dest, source1, source2)` : clone an object from `sources` to `destination`
  - `let cloneName =  structuredClone(object)` : clone most type of data, including arrays and imbriqued date such as an object into an object
  - **clone loop** : serve similair function as `Object.assign`

  ```js
    for (let key in user) {
      clone[key] = user[key];
    }
  ```

## Methods
### This
 - `this` when used in an object method, `this` refers to the `object` it is used in
  
  ```js
    const person = {
  firstName: "John",
  lastName : "Doe",
  id       : 5566,
  fullName : function() {
    return this.firstName + " " + this.lastName; //this refers to person, it is equal to person.firstName and person.lastName
   }
  }
  ```
### String
### Number
### Array
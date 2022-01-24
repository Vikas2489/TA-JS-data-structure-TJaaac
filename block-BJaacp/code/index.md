1. What will be the output and explain the reason.

```js
let obj = { name: 'Arya' };
obj = { surname: 'Stark' };
let newObj = { name: 'Arya' };
let user = obj;
let arr = ['Hi'];
let arr2 = arr;
```

Answer the following with reason after going through the above code:

- `[10] === [10]` false (whenever we use square brackets to create an array, which is non primitive type of object then,  their address will be different.)
- What is the value of obj? // { surname: 'Stark'};
- `obj == newObj` false
- `obj === newObj` false
- `user === newObj` false
- `user == newObj` false
- `user == obj` true
- `arr == arr2` true
- `arr === arr2`true


2. What's will be the value of `person1` and `person2` ? Explain with reason. Draw the memory representation diagram.

<!-- To add this image here use ![name](./hello.jpg) -->

```js
function personDetails(person) {
  person.age = 25;
  person = { name: 'John', age: 50 };
  return person;
}
var person1 = { name: 'Alex', age: 30 };
var person2 = personDetails(person1);
console.log(person1);  { name: 'Alex', age: 30 }; 
//  Because, as person1 is already defined.It will create a memory on a different address.
console.log(person2); { name: 'john', age: 25 };  
// Because of the function, age will get updated.  
```



3. What will be the output of the below code:

```js
var brothers = ['Bran', 'John'];
var user = {
  name: 'Sansa',
};
user.brothers = brothers;
brothers.push('Robb');
console.log(user.brothers === brothers); // true (As user.brothers = brothers; will add a new key to the user and this will add an element to the array of brothers key, brothers.push('Robb'); that's why it will be true.)
console.log(user.brothers.length === brothers.length); //2. true (As it is said in the above statment, that's their length will be same.)
```


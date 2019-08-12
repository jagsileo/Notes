Refer to ES6 repo -> code -> app -> index.js for code demo

### History  
No strict types, all variables are declared with var  
We use semicolons to end a command or a line  
Camel casing or snake casing for variable names

#### Functions
```
function <function_name()> {

}  
```  
Or we can assign function to a variable

```
var multiply = function(a, b) {  
    return a*b;  
}  
```  

#### JS Objects
Like map but keys are not enclosed in quotation marks  
For e.g.,  
```  
var dog = {  
    name: 'Buddy',
    breed: 'Golden Retriever',
    bark: function() {
        console.log("Woof!");
    }
}  
```

#### Arrays  
```  
var arr = [2,45,6,7,31];
points.push(8);  
var last = points.pop();  
```  
Indexes start from 0


### ES6

##### Transpilers
- Reads code written in one language and produces the equivalent code in another  
    -- CoffeeScript and TypeScript are not supported by many browsers. Transpilers convert them to vanilla JS  
    -- BabelJS.


##### WebPack
- Bundler for JS - bundles multiple files into one JS file  
- Comes with a dev server, local dev scheme with live code updating with just one line of code  

```  
npm i webpack@4.12.0 webpack-cli@3.0.3  
```

webpack@4.12.0 - actual webpack
webpack-cli@3.0.3 - use webpack in cmd line
--save-dev - we need them only for development so we ignore them when shipping code to production  
**webpack.config.js** will direct webpack on how to behave  

###### Note:  
If we could webpack-dev-server to run the code whenever there is a change without having to type npm run start

#### ES6 syntax  
Introduction of let and const is done in ES6  
let is equivalent to var  
const is a constant, anything declared as const cannot be modified  
``` 
const limit = 100;  
limit += 10; //error
```
array.push works on const  
This is because JS does not want a const to reassigned or redeclared. Its okay with adding another element to an already assigned and declared const  

##### Block Statements  
Brings out the difference between var and let  

##### Template Literals
Enables ability to embed strings. They are declared using back ticks \`\`

```
let a = `good`;
let greeting = `${a} morning`;
console.log(greeting);
```  

#### Operating and Destructuring  
###### Spread Operator  
Spread the elements in one array in another array  
```
let a = [20,30, 40];   
let b = [10, ...a, 50];   
console.log(b);
```
###### Rest Parameter
We can pass multiple parameters to a function by just passing one rest parameter  
```
function collect(...a) {
    console.log(a);
}

collect(3, 6, 9, 12, 15);
```

###### Destructing assignment  
Lets you declare array values or object entried to variables in a less verbose manner  
```
let animals = ["lion", "tiger", "zebra"];
let [a, b] = animals;
console.log(a, b); // prints lion, tiger
```

#### Modules and methods  
###### Arrow functions  
Anonymous functions mostly used in helper functions that is used only once  

###### Helper methods  
map & filter methods  

###### Map method  
Maps the function to every element of the array and returns the updated array

###### Filter method
Filters the array by applying a function over the elements of an array  

###### Helper methods  
string.repeat(count) => returns concatenates the string count times and returns the concatenated string
string.startsWith(strA) => checks whether string is prefixed by strA  
string.endsWith(strB) => checks whether string is suffixed by strB  
string.includes(str) => checks whether string has a substring str  
number.isFinite() => number type checking can occur through the method  
number.isSafeInteger() => number safety checking can occur through the method  

### Modules  
Reusable pieces of code within our application  

### Classes  
A group with some particular properties and actions  
Classes have constructor where we initialize the values for the properties. We can define methods that also can use those properties as template strings

##### extends keyword  
Inherit from a class and act as a child class  

##### Static Methods  
Implement methods without explicitly creating an instance of the class  
That way a class can act as a collection of helper methods  

### Prototypes  
Similar to OOP, prototype describes a characteristic of a JS object 
Classes are extractions on top of JS prototypes  
A prototype reveals an object's parent  
All objects - Arrays, Dates etc - have a prototype, the parent of all could be Object  
Classes aren't classes at all but prototypes under the hood



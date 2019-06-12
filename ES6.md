###History  
No strict types, all variables are declared with var  
We use semicolons to end a command or a line  
Camel casing or snake casing for variable names

####Functions
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

####JS Objects
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

####Arrays  
```  
var arr = [2,45,6,7,31];
points.push(8);  
var last = points.pop();  
```  
Indexes start from 0


###ES6

#####Transpilers
- Reads code written in one language and produces the equivalent code in another  
    -- CoffeeScript and TypeScript are not supported by many browsers. Transpilers convert them to vanilla JS  
    -- BabelJS.


#####WebPack
- Bundler for JS - bundles multiple files into one JS file  
- Comes with a dev server, local dev scheme with live code updating with just one line of code  

```  
npm i webpack@4.12.0 webpack-cli@3.0.3  
```

webpack@4.12.0 - actual webpack
webpack-cli@3.0.3 - use webpack in cmd line
--save-dev - we need them only for development so we ignore them when shipping code to production  
**webpack.config.js** will direct webpack on how to behave  

######Note:  
If we could webpack-dev-server to run the code whenever there is a change without having to type npm run start

####ES6 syntax  
Introduction of let and const is done in ES6  
let is equivalent to var  
const is a constant, anything declared as const cannot be modified  
``` 
const limit = 100;  
limit += 10; //error
```
array.push works on const  
This is because JS does not want a const to reassigned or redeclared. Its okay with adding another element to an already assigned and declared const  



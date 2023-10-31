# Day 1

## VARIABLES IN JAVA

In js the variable type can be changed during Runtime(Dynamically typed language) 

## Datatype in js

### let 
***
- used to declare block scoped variable.
- can be updated but cannot be redeclared.  
eg.


`let a=10`     
`let a ="abc"`  it display an error message
                 
but can use like this   
`let a=10 `    
`a="abc"`

### var 
***

- was earlier used before ES6 but due to some reason bugs was occuring in the code so now a days it is not used.
- can be updated and redeclared within its scope.

### const  
***  

 - used to declare constants, identifiers who's value cannot be changed throughout the program.
- cannot be updated or redeclared throughout the program.

eg.

if const `author = "name"`  
        `let author = 5`  it throws an error because the variable is declared as constant
- it has to be initialized when it is declared.
  (eg. 
  `const a;` it will throw an error to initialize it.)

**try to use const maximum.**


#### Syntax
***

datatype variable_name = value

#### Rules to naming a variable
***

- Cannot start with numbers (eg.`let 1a=12 `is not allowed)
- Can begin with letters, special character 
- Cannot use keyword as variable_name
- Case sensitive


## PRIMITIVE DATATYPE

There are 7 primitive datatype
   - N -- Null
   - N -- Number
   - S -- Symbol
   - S -- String
   - B -- Boolean
   - B -- BigInt
   - U -- Undefined  


`let a = null;`   
`let b = 156;`   
`let c = "Hello";`   
`let d = Symbol("This is a symbol");`  
`let e = true;`
`let f = BigInt("465");`   
`let g = undefined; or let g;`  it will display undefined in console 
`console.log(a,b,c,d,e,f,g);
 console.log(typeof(f))`  typeof(variable_name) is used to check the variable type.


 ## OBJECTS

 Objects are key value pairs, non primitive datatypes 

eg.  
`let person{
   name:'jhon',
   age:20
   }`  
name,age is key and jhon and 20 is value

eg.  
`const item = {
    "abc" : null,
    "xyz" : true,
    "klm" : "Hello",
    "hij" : 56,
    "pqr" :undefined
};
console.log(item["klm"])`
if we try to print an undefined key then it will dispaly undefined
eg.  
`console.log(item["rst"])`


## Practice Questions

1.Create a variable of type string and try to add a number to it

 
`let a = "Hello" `  
`let b =5`  
`console.log(a+b)`

o/p -- Hello5

2.Use typeof() operator to find the datatype of string in last question
 
`console.log(typeof(a+b))`

o/p -- string

3.Create a const object in javascript can you change it hold a number later

`const a1 = {
    name : "abc",
    class : 10,
    isFail : false
}`  
`a1=54`


o/p -- Uncaught TypeError: Assignment to constant variable.

4.Try to add a new key to the const object in problem 3,were you able to do it?

`a1['friend'] = "xyz"`  
`console.log(a1)`


o/p -- {name: 'abc', class: 10, isFail: false, friend: 'xyz'}

**Note:Can change the key value**

`a1['name']="lmn"`  
`console.log(a1)`

o/p -- {name: 'xyz', class: 10, isFail: false}

5.Write a js program to create a word-meaning dictionary of 5 words

`const dict = {   
appreciate:"recognize the full worth of.",
bipolar:'having or relating to two poles or extremities.',
colleague:'a person with whom one works in a profession or business.',
definitely:'without doubt (used for emphasis).',
empathy:'the ability to understand and share the feelings of another.'
}
console.log(dict)`

o/p -- {appreciate: 'recognize the full worth of.', bipolar: 'having or relating to two poles or extremities.', colleague: 'a person with whom one works in a profession or business.', definitely: 'without doubt (used for emphasis).', empathy: 'the ability to understand and share the feelings of another.'}

To access individual key value

`console.log(dict.colleague) or console.log(dict['colleague'])`

o/p -- a person with whom one works in a profession or business.
*** 
# Day 2

## EXPRESSIONS ANS OPERATORS

### Arithmetic operators 

  - `+`
  - `-`
  - `*`
  - `**` Exponential
  - `%`
  - `/` 
  - `++`
  - `--`

eg.

`console.log(2**3**2)`   
 o/p - 512   
first it will do 3 power 2= 9 then 2 power 9= 512

`console.log((2**3)**2)`  
o/p -  64  
first it will do 2 power 3 = 8 which is inside () then 8 power 2

`console.log(4%3**2)`  
o/p - 4
first it will do 3 power 2 = 9 then 4%9=4

`let a = 10;
console.log(a++)`  
o/p - 10

`let a = 10;
a++;
console.log(a)`  
o/p - 11

`let a = 10;
console.log(++a)`  
o/p - 11

pre increment/decrement -- first inc/dec then assign the value to variable
eg.  
++a,--b etc

post increment/decrement -- first assign the value to variable then inc/dec 
eg.  
++a,--b etc

### Assignment operators

- =   x=y
- +=  x=x+y
- -=  x=x-y
- *=  x=x*y
- /=  x=x/y
- %=  x=x%y
- **= x=x**y

### Comparision operators

- ==   equal to 
- ===  equal value and type
- !=   not equal to
- !==  not equal value or equal type
- >    greater then
- <    less then
- <=   less then or equal
- >=   greater then or equal
- ?    turnary operator

eg.   
 
`const a=6; const b="6";
console.log(a==b);
console.log(a===b)`   

o/p - true  it will return true because value is same 
      false it will return false because type is different (both value and type should be same)

### Logical operators

- &&
- ||
- !

### Comments
- // single line comment
- /*  */   multiline comment

## Conditional statements

### if statement

`if(condition){
    statement;
}`

### if...else statement

`if(condition){
   true statement;
}  
else{
  false statement;
}`


### if...else if...else statement

`if(condition 1){
     statement 1;
}else if(condition 2){
  statement 2;
}else{
  false statement;
}`

### Switch statement
`const expr = value2; `
`switch(expr){
  case value1:
  statement
  break;
  case value2:
  statement
  break;
  default:
  statement
  
}`


### Turnary Operator 


`condition ? exprIfTrue : exprIfFalse`



### prompt

it ask something from the user.

`prompt("What is your name?")`


### alart

it tells something to the user

`alert("error occured..!")`

## TypeCasting

`let a;
a = Number.parseInt(a)`
      




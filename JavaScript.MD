# Day 1

## VARIABLES IN JAVA SCRIPT

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
```
let a = null;  
let b = 156;  
let c = "Hello";
let d = Symbol("This is a symbol");  
let e = true;
let f = BigInt("465");   
let g = undefined; or let g;
```  
it will display undefined in console 
```
console.log(a,b,c,d,e,f,g);
console.log(typeof(f))
 ``` 
  typeof(variable_name) is used to check the variable type.


 ## OBJECTS

 Objects are key value pairs, non primitive datatypes 

eg.  
```
let person{
   name:'jhon',
   age:20
   }
   ```  
name,age is key and jhon and 20 is value

eg.  
```
const item = {
    "abc" : null,
    "xyz" : true,
    "klm" : "Hello",
    "hij" : 56,
    "pqr" :undefined
};
console.log(item["klm"])
```
if we try to print an undefined key then it will dispaly undefined
eg.  
`console.log(item["rst"])`


## Practice Questions

1.Create a variable of type string and try to add a number to it

 
```
let a = "Hello"   
let b =5
console.log(a+b)
```

o/p -- Hello5

2.Use typeof() operator to find the datatype of string in last question
 
`console.log(typeof(a+b))`

o/p -- string

3.Create a const object in javascript can you change it hold a number later

```
const a1 = {
    name : "abc",
    class : 10,
    isFail : false
}  
a1=54
```


o/p -- Uncaught TypeError: Assignment to constant variable.

4.Try to add a new key to the const object in problem 3,were you able to do it?

```
a1['friend'] = "xyz"  
console.log(a1)
```


o/p -- {name: 'abc', class: 10, isFail: false, friend: 'xyz'}

**Note:Can change the key value**

```
a1['name']="lmn"
console.log(a1)
```

o/p -- {name: 'xyz', class: 10, isFail: false}

5.Write a js program to create a word-meaning dictionary of 5 words

```
const dict = {   
appreciate:"recognize the full worth of.",
bipolar:'having or relating to two poles or extremities.',
colleague:'a person with whom one works in a profession or business.',
definitely:'without doubt (used for emphasis).',
empathy:'the ability to understand and share the feelings of another.'
}
console.log(dict)
```

o/p -- {appreciate: 'recognize the full worth of.', bipolar: 'having or relating to two poles or extremities.', colleague: 'a person with whom one works in a profession or business.', definitely: 'without doubt (used for emphasis).', empathy: 'the ability to understand and share the feelings of another.'}

To access individual key value

```
console.log(dict.colleague) or console.log(dict['colleague'])
```

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

```let a = 10;
console.log(a++)
```  
o/p - 10

```let a = 10;
a++;
console.log(a)
```  
o/p - 11

```let a = 10;
console.log(++a)
```  
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
 
```
const a=6; const b="6";
console.log(a==b);
console.log(a===b)
```   

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

```
if(condition){
    statement;
}
```

### if...else statement

```
if(condition){
   true statement;
}  
else{
  false statement;
}
```


### if...else if...else statement

```
if(condition 1){
     statement 1;
}else if(condition 2){
  statement 2;
}else{
  false statement;
}
```

### Switch statement
```
const expr = value2; 
switch(expr){
  case value1:
  statement
  break;
  case value2:
  statement
  break;
  default:
  statement
}
```


### Ternary Operator 


`condition ? exprIfTrue : exprIfFalse`



### prompt

it ask something from the user.

`prompt("What is your name?")`


### alart

it tells something to the user

`alert("error occured..!")`

## TypeCasting

```
let a;
a = Number.parseInt(a)
```
      
### practice questions

1.Use logical operator to find weather the age of a person lies b/w 10 and 20

```
const age= 25;
if(age>=10&&age<=20){
  console.log("true");
}else{
  console.log("false");
}
```

2.Demonstrate the use of switch statement in js.

```
const expr = "Hello";
switch(expr){
  case "hello":
    console.log("match 1");
    break;
  case "Hello":
    console.log("match 2");
    break;
  defaule:
    console.log("invalid");
}
```

3.Write a javascript prg to find weather a no dividible by 3 and 2

```
const num = 55;
if(num%3==0 && num%2==0){
  console.log("true");
}else{
  console.log("false");
}
```


4.Write a js prg to find whether a no is divisible by 2 or 3.

```
const num = 45;
if(num%3==0 && num%2==0){
  console.log("div by both");
}else if(num%3==0 ){
  console.log("div by 3");
}else if(num%2==0){
   console.log("div by 2");
}else{
  console.log("false");
}
```

5.Print "You can drive" or "you cannot drive" based on age being greater then 20 using ternary operator.

```
const age=25;
age>=20?console.log("you can drive"):console.log("you cannot drive")
```



# Day 3

## Loops

- for loop
- while loop
- do..while loop
- for..of loop  -- loop through the value of an object
- for..in loop  -- loop through the keys of an object

### for loop

Syntax:
  

for(initialization;condition;inc/dec){
  statement block
}
  

### for in loop

Syntax:

for(datatype variable_name in object_name){
  statement
}

eg.

```
let marks = {
  Kannada:95,
  Engilsh:90,
  Maths:92
}
for(let a in marks){
  console.log(a+"   "+marks[a]);
}
```
o/p -   
Kannada   95  
Engilsh   90  
 Maths   92

*** Note: for in loop also work with array. ***


### for of loop

Syntax:

for(datatype variable_name of object_name){
  statement
}

```
let marks = [50,10,54,77]
for(let a of marks){
  console.log(a);
}
```
o/p -   
 50  
 10  
 54  
 77  

*** Note: for of loop doesn't used to manipulate the values of an object. *** 
 

### while loop

Syntax:

while(condition){
  statement execute untill the condition is satisfied
}

### do..while loop


Syntax:

do{
  Statement;
}while(condition);


## Functions

Syntax:

function function_name(arguments){
  statements
}

or 

By using arrow function


eg.

```
const sum = (p,q)=>{
  return p+q;
}
console.log(sum(10,10))
```

-we can also create default function which does not contains arguments.


### Practice Question

1.Write a prg to print the marks of a students in an object using for loop.

```
let marks = {
  tom:90,
  jerry:95,
  Naruto:50,
  sasuke:90
}
for(let i=0;i<Object.keys(marks).length;i++){
   console.log(" marks of "+Object.keys(marks)[i]+" is "+marks[Object.keys(marks)[i]])
}
```

2.Write the previous prg using for in loop.

```
let marks = {
  tom:90,
  jerry:95,
  Naruto:50,
  sasuke:90
}
for(let a in marks){
  console.log(a+" marks is "+marks[a])
}
``` 

3.Write a prg to print "try again" until the user enter the correct no.

```
 let a;
  num = Number.parseInt(a);
  while(a!=5){
    console.log("Try again..."); 
    a= prompt("Enter the no");
  }
  console.log("Correct no");
```

or


```
let flag = true;
  while(flag){
    let a;
a= prompt("Enter the no"); 
  num = Number.parseInt(a);
    if(num===5){
      flag=false;
      console.log("congrats...!");
    }else{
      console.log("try again...!")
    }
  }
  ```

4.Write a function to find a mean of 5 no.

```
function mean(a,b,c,d,e){
      return (a+b+c+d+e)/5;
}
mean(10,15,2,5,4);
```

or 

```
const mean = (a,b,c,d,e)=>{
  return (a+b+c+d+e)/5;
}
mean(10,15,2,5,4);
```


## Strings

- which is written inside single quots,double quotes.
- string or immutable.

eg.    

 `let name = "Tom"`  
`let nsme1 = 'Jerry'`

Another method using backtick(``)

Template Literals

eg.

```
let boy1 = "Tom"
let boy2 = 'Jerry'
let sentance =  `${boy1} is a friend of ${boy2}`
```

-inside backtick we can use single quotes as well as double quotes
-The above example is also calleds **string Interpolation** --we can directly variable inside templete literals.

### Escape Sequence Character

- \ -- is escape sequence character.
- used to include single quote (') or double quote (") in the string
  
  eg.
  ```
  let a= 'doesn\'t'
  console.log(a)
  ```

other escape sequence character
- \n -- new line
- \t -- tab
- \r -- carriage return (Gives the position of ( \ ) in the string).

## String Methods

- length
- toUpperCase()
- toLowerCase()
- slice(start_index,end_index) **Note : end_index is not included**
- replace("existing_word","new_word")
- concat("arg1",arg2,arg3,....)
- trim()

### practice Question

1.What will the following print in js?
```console.log("har\"".length)```

o/p -- 4

2.Explore the includes starts with and ends with function of a string.

```
const sen = 'The quick brown fox jumbs over the lazy dog.'
const word = 'fox'
console.log(`The word " ${word} " ${sen.includes(word)? 'is' : 'is not'} in the sentence ` )
```

o/p -- The word " fox " is in the sentence 


3.Write a prg to convert given string to lowercase.


```
let str = "Hello World!"
console.log(str.toLowerCase())
```

o/p -- hello world!


4.Extract the amount out of this string.
` Please give Rs 1000`

```
let sen1="Please give Rs 1000"
let amt = Number.parseInt(sen1.slice(15)) 
console.log(amt)
```

5.Try to change 4th character of a given string .

```
let sen2 = "Please give Rs 1000"
let res = sen2.replace('a',4)
console.log(res)
```
o/p -- Ple4se give Rs 1000


** Note : but we cannot change existing string
```
let sen2 = "Please give Rs 1000"
sen2[4]="r"
console.log(sen1)
```
o/p -- Please give Rs 1000


# Day 4

## Arrays

- In js array are object(The typeof() opertor on array return object)
- We can store differnt type of elements(eg. in a array we can store string,number,character,null,so on...)
- If we try to access a index number which is greater then array length it will display undefined

Syntax:

data_type array_name = [val1,val2,val3....]

### Array Methods

- toString() -- (Used to convert array to string)
- join("val") -- (it is used to join the val between each elements,it replaces the comma by val it converts the array into string automatically)
- pop() -- (Remove the last element,returns the poped element eg. let a = arr.pop() -- a will store the removed elements)
- push(val) -- (Add the val at end,return the new length of the array eg. let a = arr.push(9) after 9 is added to the array it returns the new length of array in the variable a)
- shift() -- (similar to pop() but removes the element at begining)
- unshift() -- (similar to push() but adds the element at begining)
- delete -- its an operator ,it will delete the element which is present in the specified index **but the array length does not change** eg. delete arr[0] -- the 0th element is deleted but length remains same.
- concat() -- used to add 2 or more array.
- sort() -- used to sort the array in ascending order(according to alphabets).
  Ascending sorting for numbers
  ```
  let compare = (a,b)=>{
    return a - b
  }
  let num = [10,56,45,89]
    num.sort(compare)
    console.log(num)
  ```
    Descending sorting for numbers
  ```
  let compare = (a,b)=>{
    return b - a
  }
  let num = [10,56,45,89]
    num.sort(compare)
    console.log(num)
  ```
-  reverse() -- Reverse the array.
-  splice() -- used to add new items to an array  
Syntax :   
 splice(position to add,no of elements to remove,elements to add seperated by comma)
 ```
   let num = [10,56,45,89]
  num.splice(2,3,49,56,87,91)
  console.log(num)
 ```
 o/p -- [10, 56, 49, 56, 87, 91]
 
-slice() -- slices out a piece from an array,  
        -- creates a sub array
        -- does not modify the original array.
```
let num = [10,56,45,89]
console.log(num.slice(1))
console.log(num.slice(2,3)) **does not include the ending index**
```
o/p -- [56, 45, 89]  
       [45]

### Using loops with array


- for loop
```
let a= [10,85,65,45,456]
for(let i=0;i<a.length;i++){
  console.log(a[i])
}
```

- forEach loop
- used to perform some operation on existing array  
Syntax:

```
arr.map((value,index,array)=>{
  statement
})
```

```
let a= [10,85,65,45,456]
a.forEach((ele)=>{
  console.log(ele)
})
```

- Array from -- used to create an array from any other object.
  
```
let name = "JavaScript"
let arr = Array.from(name)
console.log(arr)
```
o/p -- ['J', 'a', 'v', 'a', 'S', 'c', 'r', 'i', 'p', 't']

- for...of loop

```
let a= [10,85,65,45,456]
for(let i of a){
  console.log(i)
}
```

- for...in loop -- prints the index no.
  
```
let a= [10,85,65,45,456]
for(let i in a){
  console.log(i)
}
```

# Day 4

## map() 

- creates a new array by performing some operation on each array elements.
- Similar to forEach but used to create new array 

Syntax:

```
arr.map((value,index,array)=>{
  statement
})
```
```
let arr= [14,56,78,89]
let arr1 = arr.map((val,index,arr)=>{
  console.log(val+1,index,arr)
}) 

```
o/p --
val  index  array    
15 0 (4) [14, 56, 78, 89]  
57 1 (4) [14, 56, 78, 89]  
79 2 (4) [14, 56, 78, 89]  
90 3 (4) [14, 56, 78, 89]

## filter()

Syntax:
```
arr.filter((ele)=>{
  condition to select array elements
})
```

```
let arr= [14,56,78,89]
let arr1 = arr.filter((ele)=>{
  return ele<60
})
console.log(arr1)
```
o/p - [14, 56]

## reduce()

Syntax:
```
arr.reduce((val1,val2,val3...)=>{
    operation
})
```

```
let arr = [1,2,3,4,5]
let arr1 = arr.reduce((val1,val2)=>{
  return val1 + val2
})
console.log(arr1)
```

or
```
let arr = [1,2,3,4,5]
const con = (val1,val2)=>{
  return val1 + val2
}
let arr1 = arr.reduce(con)
console.log(arr1)
```
o/p -- 15 

steps:
- first arr[0] is added with arr[1] 
- then the result will added with arr[2]
- it keeps on repeating untill all the elements are added.

### Practice Question

1. Create an array of numbers and take input from the user to add numbers to this array.

```
let arr = [1,2,3,4,5,6,78,45]
let a= prompt("Enter a number")
a= Number.parseInt(a)
arr.push(a)
console.log(arr)
```
o/p - enter a number  
100   
[1, 2, 3, 4, 5, 6, 78, 45, 100]

2. Keep adding numbers to an array in qst1 until 0 is added to the array.

```
let a
let arr = [1,2,3,4,5,6,78,45]
do{
a= prompt("Enter a number")
a= Number.parseInt(a)
arr.push(a)
}while(a!==0);
console.log(arr)
```
o/p --   
Enter a number  
45  
Enter a number  
78  
Enter a number  
0  
[1, 2, 3, 4, 5, 6, 78, 45, 45, 78, 0]

3. Filter for no divisible by 10 from a array.
```
let arr = [1, 2, 3, 40, 5, 6, 78, 45, 450, 780, 100]
let a = arr.filter((val)=>{
    return val%10===0
})
console.log(a)
```
o/p -- [40, 450, 780, 100]

4. Create an array of square of given no.
```
let arr = [1,2,3,4,5,6,78,45]
let a = arr.map((val)=>{
  return val * val
})
console.log(a)
```
o/p -- [1, 4, 9, 16, 25, 36, 6084, 2025]

5. Use reduce to calculate the factorial of a given no from an array of first n natural no(n being the no whose factorial needs to be calculated)

```
let arr = [1,2,3,4,5]
let a = arr.reduce((v1,v2)=>{
    return v1*v2
})
console.log(a)
```
o/p -- 120
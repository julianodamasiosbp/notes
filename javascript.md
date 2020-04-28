# Javascript

#### Variable can vary;
---

	let price = 40;
	
#### Constants can not vary:
---

	const price = 40;

***Var variable is not used anymore;***

#### Naming variables:
---

	Begin with: _ $ letter

#### Types and Operators
---

	* Numbers;
	* Strings;
	* Booleans;
	* Null and undefined;
	* Objects and Symbols;

	typeof() -> Returns the type of a variable;

	price += 5

	price *= 5

	console.log(++price) -> Returns price + 1;

	console.log(--price) -> Returns price - 1;

**MDN Operator precedence**

#### Strings
---

	3 styles:
	* Single quotes ''
	* Double quotes ""
	* Backtick quotes ``

	"Hello \"World\"" -> This will show quotes on the word "World";
	
	Using backtick -> console.log(`Hello, ${name}`);
	
	message.toUpperCase()
	
	message.lenght; -> Return the size of a variable;
	
	amount.toString() -> Converting a Number into a String
	
	amount = Number.parseFloat("123.25") -> Converting a String to a Number;

#### Booleans
---

	* True;
	* False;
		
	let saved = true;
	saved = !saved; -> Return false;

#### Null and Undefined
---

	Undefined -> When a variable is not initialized, the JS return "undefined";
	Null -> Best pratice to declare a variable as null when needed;
	
#### Objects and Symbols
---

	let person = {
		firstName: 'João',
		lastName: 'Silva'
	};

	console.log(person.firstName); -> Return "João"

#### Conditionals IF
---

	if (5 === 5){
		console.log('Yes')
	};
	
	if (state !== 'RN'){
		taxPercent = 7;
	};

#### Falsy and Truthy
---

| Falsy                    | Truthy               |
|--------------------------|----------------------|
| false                    | Everything NOT falsy |
| 0                        | true                 |
| "" or '' (empty strings) | 0.5                  |
| Null                     | "0"                  |
| Undefined                |                      |
| NaN                      |                      |

	Dealing with float numbers -> (+(1.1 + 1.3).toFixed(2) === 2.4)

#### if() ... else

	if (state === 'RN'){
		taxPercent = 7;
	}
	else {
		taxPercent = 0;
	}

---
	if (state === 'RN'){
		taxPercent = 7;
	}
	else if (state === 'CE') {
		taxPercent = 8.75;
	}
	else if (state === 'SP') {
		taxPercent = 9.12
	}
#### The Ternary Operator
---
	let message = (price > 10) ? 'Expensive' : 'Cheap';
	
#### Looping with for()
---

	for (let i = 0; i < 3; i++) {
		console.log(i)
	}
---
*Decrement*

	for (let i = 5; i > -1; i--) {
    console.log(i)
}

#### while() Loop
---

	let i = 0;
	while (i < 11) {
		console.log(i);
		i++;
	}
---
*Decrement*

	let i = 5;
	while (i > -1) {
    console.log(i);
    i--;
}

#### Looping with do ... while()
---

	let i = 0;
	do {
		console.log(i);
		i++;
	} while(i < 5);

#### Functions
---

	A fucntion is a block of organized, reusable code that is used to perform a single, related action;
	
	function showMessage() {
		console.log('in a function');
	}
	
	showMessage(); -> Calling the fucntion;
	
*Function Expression*

	let fn = function(){
		console.log('in a function)
	}
	
	fn(); -> Calling the function expression;
	
---

*Passing information to Function;*
	
	function showMessages(message, anotherMessage) {
		consgole.log(message, anotherMessage)
	}
	
	showMessages('First message', 'Second message') -> Calling the function.
	
---

*Function return values;*
	
	function soma(a, b){
		let soma = a + b;
		return soma;
	}
	
	console.log(soma(7, 4)); -> Calling the function with return;

*Arrow Functions*



#### Object Properties
---

	let person = {
		name: 'João',
		age: 33,
		partTime: false
	};

	console.log(person.name) -> Return 'João';
	console.log(person['name'])

#### Object Methods
---

	let person = {
		name: 'João',
		lastname: 'Silva,
		age: 33,
		partTime: false,
		fullName: function(){
			showMessage(this.name + ' ' + this.lastname)
		}
	};
	
	person.fullName(); -> Return 'João Silva';
	
*Mozilla MDN -> Starndard Built-in Objects;*
	
#### Document Object Model (DOM)
---

	const header = document.getElementById('message');
		header.style.color = 'blue'; -> This change the color of element to blue;
	
#### Arrays
---

	let values = [];
	let values = [1, 2, 3]; -> Values has 3 elements;
	
	let values = Array.of(1, 2, 3); -> Creating a array with 3 elements;

*Array is a object, so to check if a variable is a array, there is a method -> Array.isArray()*
	
	Arrays are 0-based;
	
	values[2] -> Return '3' from values array;
	
	values[2] = '123' -> This change the '3' to '123';

	values.indexOf('1'); -> Return the position from this element;
	
	values.push('d'); -> Add a new element to the end of an array;
	
	values.push('a', 'b', 'c') -> Add 3 element to the end of an array;
	
	last = values.pop(); -> Remove the last element from the end of an array;
	
	first = values.shift(); -> Remove the first element from an array;
	
	values.unshift('a'); -> Add a new element to the begin of an array;

*slice() and splice()*

---

*slice()*
	
	const values = ['a', 'b', 'c', 'd'];
	
	const newValues = values.slice(1, 2); -> Create a new array with 2 elements ['b', 'c'];

	const newVales = vales.slice(); -> Create a copy of values array;

*splice() for Deleting*

	const values = ['a', 'b', 'c'];
	
	values.splice(1, 1); -> '1' means the position of index, second '1' means how many elements to remove;

*splice() for Inserting*

	const values = ['a', 'b', 'c'];

	values.splice(1, 0, 'foo'); -> '1' means the position of index, '0' how many elements to remove, 'foo' the new element to insert on position 1; ['a', 'foo', 'b', 'c,']

*Array Searching and Looping*

---

*filter()*

	const values = ['a', 'b', 'c'];
	const set = values.filter(function(item) {
		return item > b;
	});

	console.log(set); -> Return 'c';

*find()*
	
	const values = ['a', 'bbb', 'c'];
	const found = values.find(function(item) {
		return item.length > 1;
	});

	console.log(found); -> Return 'bbb';

*forEach()*

	const values = ['a', 'b', 'c'];
	values.forEach(function(item) {
		console.log(item);
	}); -> Return 'a', 'b', 'c'

#### Arrays in the DOM
---

	const containers = 
		document.getElementsByClassName('container');
	containers[2].classList.add('d-none');
	
	console.log(containers)

#### Scope and Hoisting
---

	-Global Scope;
	-Function Scope;

*Hoisting*

	-You can call a function before it was declared;

	showProductId();

	function showProductId() {
		console.log(123);
	}

	'use strict'; -> Use this at begin JS code to force you to declare variables;

#### Variables and Types
---

	String.raw ->

| Var                                 | Let                                | Const                                  |
|-------------------------------------|------------------------------------|----------------------------------------|
| No Block scope                      | Block scope                        | Block scope                            |
| Can be redeclared anywhere          | Can NOT be redeclared witinh scope | Can NOT be reassigned or redeclared    |
| Can be used and reassigned anywhere | Can be reassigned within scope     | The value it references CAN be changed |

*Destructing Syntax*

	before:
	    var isEmployed = la.Factors[0];
        var hasKids = la.Factors[1];
        var hasLoans = la.Factors[2];
        var hasCreditcards = la.Factors[3];

	after:
		var[
			isEmployed, 
			hasKids, 
			hasLoans, 
			hasCreditcards
		] = la.Factors;

*Refactoring*

	before:
	var nameAndTitle = la.ApplicantName;

    var indexOfMD = nameAndTitle.search("MD");
    var indexOfMD2 = nameAndTitle.search("M.D");
    var indexOfMD3 = nameAndTitle.search("M.D.");
    var indexOfPhD = nameAndTitle.search("PhD");
    var indexOfPhD2 = nameAndTitle.search("Ph.D");
    var indexOfPhD3 = nameAndTitle.search("PHD");
    var indexOfDr = nameAndTitle.search("Dr.");
    var indexOfDr2 = nameAndTitle.search("DR.");

    if (indexOfMD > -1 || indexOfMD2 > -1 || indexOfMD3 > -1 
        || indexOfPhD > -1 || indexOfPhD2 > -1 
        || indexOfPhD3 > -1 || indexOfDr > -1 || indexOfDr2 > -1) {

        risk = risk - 1;
	
	after:
	var nameAndTitle = la.ApplicantName.trim().toLowerCase();

	let dr = nameAndTitle.startsWith('dr');
	let phd = nameAndTitle.startsWith('phd');
	let phd2 = nameAndTitle.startsWith('ph.d');

	let md = nameAndTitle.endsWith('md');
	let md2 = nameAndTitle.endsWith('m.d');
	let md3 = nameAndTitle.endsWith('m.d.');

	if (dr || phd || phd2 || md || md2 || md3) {
        risk = risk - 1;
	}


#### Syntax and Operators
---
*Switch statement*

	let productId = 2;

	switch (productId) {
		case 1:
			console.log('Product 1');
			break;
		case 2:
			console.log('Product 2');
			break;
		default:
			console.log('Unknown product');
			break;
	}
	- Do NOT forget to put 'break' in each case;

*Using switch case with blocks;*

	let productId = 2;

	switch (productId) {
		case 1: {
			let message = 'foo';
			console.log(message);
			break;
		}
		case 2: {
			let message = 'bar'
			console.log(message);
			break;
		}
	}

*For/in Statement*

	for (const key in product) {
		console.log("'" + key + "'=" + product[key]);
	}

*For/of Statement*

	let productName = 'HL Road Frame - Black, 58'
	let letters = '';

	for (const char of productName) {
		letters += char;
	}
	
	console.log(letters);

*Break and Continue Statements*

	- Break statement -> "jumps out" of a loop;
	- Continue statement -> "jumps over" one iteration in the loop;

*Labeled Statement*
	
	- Define a location to "goto";
	- Not recommended for use;
	
#### Mathematical Operators
---

	- Addition (+) 2 + 3
	- Substration (-) 4 - 2
	- Multiplication (*) 3 * 2
	- Division (/) 8 / 4
	- Exponentiation (**) 2 ** 2
	- Modulus (%) 9 % 4
	- Increment (++) index++
	- Decrement (--) index--

*Converting String to Number*

	let price = 200;
	let stringValue = '100';
	let result = 0;
	
	result = price + stringValue;
	console.log(result) -> Return 200100
	
	result = price + (+stringValue);
	console.log(result) -> Return 300;
	
*Assignment Operators*

	- Equal (=) price = 10;
	- Addition (+=) price += 5;
	- Substration (-=) price -= 2;
	- Multiplication (*=) price *= 3;
	- Division (/=) price /= 1.5;
	- Exponentiation (**=) price **= 2;
	- Modulus (%=) price %= 4;
	
*Comparison Operators*
	
	- Less than (<) price < 10;
	- Less than or equal to (<=) price <= 10;
	- Greater than (>) price > 10;
	- Greater than or equal to (>=) price >= 10;
	- Equal in value (==) price == 10;
	- Equal in value and type (===) price === 10;
	- Not equal in value (!=) price != 10;
	- Not equal in value and type (!==) price !== 10;
	
*Logical Operators*
	
	- And (&&) price > 10 && price < 1600;
	- Or (||) price > 10 || price < 1400;
	- Not (!) !(price > 10);

*Short Circuiting*
	
	&& -> If first result is false, all the rest is never evaluated;
	|| -> Each expression is evaluated until one returns a true;

#### Javascript Exception Handling
---

	try {
		// Some code that could fail
	}
	catch (error) {
		// Do something with the error
	}
	finally {
		// This code always runs
	}

*Throw*

	- The throw statement allows you to create a custom error;
	
	try {
    if(x == "") throw "is Empty";
    if(isNaN(x)) throw "not a number";
    if(x > 10) throw "too high";
    if(x < 5) throw "too low";
  }
  
	catch(err) {
    message.innerHTML = "Input " + err;
  }

#### Types of Erros
---

	- ReferenceError;
	- RangeError;
	- TypeError;
	- URIError;
	- SyntaxError;
	- EvalError;

#### Object Data Type / Constructor
---

	- typeof
	- instanceof -> The instanceof operator tests the presence of constructor.prototype in object's prototype chain.

#### 'This' in Javascript
---

	- Refers to an object;
	- call and apply are very similar—they invoke a function with a specified this context, and optional arguments. 
		The only difference between call and apply is that call requires the arguments to be passed in one-by-one, and apply takes 
		the arguments as an array.
		
	const book = {
		title: 'Brave New World',
		author: 'Aldous Huxley',
	}

	function summary() {
		console.log(`${this.title} was written by ${this.author}.`)
	}

	summary.call(book) -> Return "Brave New World was written by Aldous Huxley."

	summary.apply(book) -> Return "Brave New World was written by Aldous Huxley."

#### Spread Operator
---

	- Expand any 'iterable' such as a string or array into an array;
	- The syntax uses the ellipsis symbol (...);
	- Always on the right-side of an equal sign;
	- Used to copy an array:
	
	let lista = [1, 2, 3];
	let lista2 = [...lista];
	
*Concatenate two arrays*

	let allProducts = [..._products, ...newProducts];

*Passing parameters to a function*

	function multipleParams(arg1, arg2, arg3) {
		console.log(arg1);
		console.log(arg2);
		console.log(arg3);
	}
	
	let args = [1, 2, 3];
	
	multipleParams(1, 2, 3);
	or 
	multipleParams(...args);

*Shallow Copy on object literals*

	let product = {
		productID: 680,
		name: 'HL Road Frame',
		standardCost: 1059.31
	};
	
	let prod2 = { ...product }; -> Shallow copy from product;

#### Arrays and Collections
---

	- Data Collection -> Stores and structures large amounts of data types for easy access;
	- Arrays, Objects, Sets, Maps, WeakSets, WeakMaps;
	- Primitives Data types -> Boolean, Null, Undefined, Number, BigInt, String, Symbol;
	- Structural Data type -> Object;

*Sets*

	- Each value in the Set has to be unique;
	- Store values of any types, whether primitive values or object references;
	- const mySet = new Set(); -> Creating a Set;
	- mySet.add('1500'); -> Add new element to Set;
	- mySet.delete('1500'); -> Delete '1500' from Set;
	
*WeakSet*

	- Only contain objects;
	- No primitive data types;
	- Not iterable;
	- No access to size property;
	- Garbage collected;
	- Methods: Add, Delete, Has;
	
	const categories = new WeakSet();
	
	let running = {category: 'Running'};
	categories.add(running));

*Maps*

	// Add notes here;
	
*WeakMap*

	// Add notes here;
	
*Typed Arrays*

	let productBuffer = new ArrayBuffer(16);
	
	let view1 = new Int8Array(productBuffer);
	
	view1[0] = 32;
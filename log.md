# 100 Days Of Code - Log

### Day 20 - 6th November 2020 ~ Headachey, ennui

Writing long function with a lot of `if` statements to get the display correct.


### 5th November 2020 - Day 19

Created Trello for Stopwatch. Split out functions for increment and displaying 0s.

### 3rd November 2020 - Day 18

Added 0 to CS.


### 29th October 2020 - Day 17

Current Stopwatch bugs:

- clearInterval() not working
- Clicking Start more than once speeds up the clock
- 0 isn't added to numbers below 9 for cs


### 28th October 2020 - Day 16

Using `this` keyword in an object method and then calling that function outside of the object doesn't seem to work. If I change `this` to the name of the object then it works.

If you assign a function to a variable, adding parentheses to said function will invoke the function. If you just want to assign it to the function without invocation, miss out hte parentheses.

### 27th October 2020 - Day 15

Worked on the stopwatch all fucking day.

### 26th October 2020 - Day 14

Pushed the code I'd worked on on laptop to Github using command line. Remote repo on Github MUST be made in Github however, it cannot be created from the command line. Then downloaded it to the desktop to work on.

Worked on stopwatch. I think laying it out as an object should be the way forward. Others seem to use the setTimeout() method but I can only understand it using the setInterval() method at the moment. This one is the most straightforward one so far: https://jsfiddle.net/Daniel_Hug/pvk6p/



### 22nd October 2020 - Day 13

Ran through switch/case statements in FCC. Also a reminder that in a function, a statement using comparisons will evaluate to either true or false. This allows you to shorten if/else statements that return a boolean value.

Functions in Javascript are essentially Objects. Like Objects, they can be assigned to variables, passed to other functions and returned from functions.

**Idea for program - Take entire text from log and arrange in reverse so latest entries are at the top.**

### 19th October 2020 - Day 12

Completed 4 hour C++ training vid. Stuff I remember - case/switch is the same. Mainly, the course helped to concrete better understanding of OOP. Javascript seems similar here.


### 14th October 2020 - Day 11

Stopwatch - Create a new date, then use getTime() function. Then update every millisecond with current time -minus original time.

```js
var purpose = function seek(desire) {
        if (desire) { 
            seek();
          }
        else {
            seek();
          }
        }
```


### 12th October 2020 - Day 10

Next project - Stopwatch. Use the date() object to get the hours, minutes, seconds and milliseconds. It will have a Start, Stop and Reset button.

Start = Display hours, minutes, seconds and milliseconds, updating in realtime upon clicking
Stop = Stop the time from advancing upon clicking
Reset = Display 00:00:00 and advance again.


### 11th October 2020 - Day 9

Going back to comparisons with objects, you may not see the results you expect due to objects being held in reference. This means that the values are stored in memory somewhere on the PC, then a reference to that location is stored in the object variable. So if you strictly compare to arrays that contain the same values, you will receive a false result due to the fact that it's their locations that are being compared, not their actual values.

**Dynamic Typing** means that variable values can be changed later in the code. For example:

```JS
let name = "Natasha";
console.log(typeof name);       //string
let name = 14;
console.log(typeOf name);       //number
```

The example above kept throwing an error that there was a missing ). However, it turns out that `typeof` **does not use camelCase**. This is because typeof is an operator (as well as instanceof). Reserved words do not follow camelCase.

#### Classes

Classes are used as blueprints to create other objects. 


### Virtual Dice - Project Completed

Classes allow object-oriented programming by creating a class which you can then create objects from. The `extends` keyword then allows you to make child classes from a parents. `super` allows you to inherit a method from the parent class for use in a child class. Both inherited and overwridden methods can exist with the same name; this is called *Polymorphism*.

### 10th October 2020 - Day 8

Finished off comparison operators in FCC and read about taking care with coercion in YDKJY. Reached "How we Organise in JS" and am stuck with these concepts. In fact I haven't learned this at all previously. I need to go over *Classes* (and perhaps Object Oriented Programming in general) and the `this` keyword https://www.w3schools.com/js/js_this.asp.



### 9th October 2020 - Day 7

If statements will evaluate whether a condition inside a function is true. If so, it will do something. If not, it can do something else. Example:

```js
function isThisTrue(value) {
    if (value) {
        return "This is true";
   }
    return "This is false";
   }
```
You can have multiple ifs like so:

```js
function greaterThan(value) {
    if (value > 100) {
        return "Greater than 100";
    }
    if (value > 10) {
        return "Greater than 10";
    }
    return "It's small.";
    }
```

Continuing on from yesterday's comparison operators:

```==```    equal value
```===```   equal value and equal type

For Javascript to compare two datatypes, it must convert one type to another. This is called *Type Coercion*. This way, 3 can `===` "3", but 3 cannot `===` "3". *Coercion* doesn't take place when using `===`.

The inequality operator `!=` also performs *coercion*. As above, the strict inequality operator `!==` does not.

```js
1 != 2      // true
1 != "1"    // false

3 != "3"    // true
3 != 3      // false
```

### 8th October 2020 - Day 6

The ```===``` comparison does not necessarily mean exactly equal. It doesn't work witn Nan or -0. It's recommended to use ```Object.is()``` which could be colloquially known as the four equals ```====``` operator - really really strict.

```===``` Also does not work with arrays due to some stuff about object values being held by reference. Further reading is needed to understand this and it's covered in Appendix A.

Went back over functions. Reached https://github.com/LonelyOrphan/You-Dont-Know-JS/blob/2nd-ed/get-started/ch2.md#coercive-comparisons



### 7th October 2020 - Day 5

#### Functions:

Function Declaration is different from a Function Expression.

Function Declaration - appears as a statement by itself, NOT as an expression in another statement. The association between the identifier awesomeFunction and the function value happens during the compile phase of the code, before that code is executed.

```js
function awesomeFunction(coolThings) {
// ..
return amazingStuff;
}
```

Function Expression - This function is an expression that is assigned to the variable awesomeFunction. Different from the function declaration form, a function expression is not associated with its identifier until that statement during runtime.

```js
// let awesomeFunction = ..
// const awesomeFunction = ..
var awesomeFunction = function(coolThings) {
// ..
return amazingStuff;
};
```

It's extremely important to note that in JS, functions are values that can be assigned (as shown in this snippet) and passed around. In fact, JS functions are a special type of the object value type.

When putting <script></script> tags on a webpage, put it down the bottom of the HTML  as it will load the content first which will make the page load faster for the user.
    
Remember to call your function in order to get it to run. Example:

```js
    function go(){
        alert("Hi!);
        alert("Hi again!);
    };

go();
go();   //function is called twice
```

Function parameters work like so:

```js
function greeting(myName) {
    console.log(`Hello ${ myName }`);
    }
    
greeting("Natasha");    // Hello Natasha
```

Use the ```return``` keyword to return a value. You can only return a single value, so if you have more values to return, wrap them up in an *Object* or *Array*.

JS parameters are the aliases for the values passed into the function. Arguments are the actual values themselves. Below, a, b and c are the parameters, while Hello, It's Me, How are you? are the arguments.

```js
var foo = function(a, b, c) {
    alert(a);
    alert(b);
    alert(c);
    };                                      // Parameters
    
foo("Hello", "It's me", "How are you?");    // Arguments
```

A note about Scope:

Variables that are declared without using the ```var``` keyword are automatically created in the Global Scope.

Global Scope: Visible everywhere
Local Scope: Visible only within the function

### Day 4.5

Read "The Web Rules Everything About (JS)" chapter. Start from "Not All (Web) JS..."


What I've learned - Not all functions are included in the Javascript specification, such as alert(), fetch(), console.log() etc. So these are more like "guests", that are still Javascript but aren't part of the specification. To check if something is "official" Javascript, check the specification, as it may be something that is included in the browser.

There are various paradigms in programming, and some languages must stick to their paradigm. Javascript is multi-paradigm and has a lot of flexibility. It might be worth reading more about programming paradigms:

https://www.freecodecamp.org/news/what-exactly-is-a-programming-paradigm/

Javascript is backawards compatible. This means that once something is accepted as valid JS, there will not be a future change to the language that causes that code to become invalid JS. Code written in 1995—however primitive or limited it may have been!—should still work today.

It is not forwards compatible. Being forwards-compatible means that including a new addition to the language in a program would not cause that program to break if it were run in an older JS engine.

https://github.com/getify/You-Dont-Know-JS/blob/2nd-ed/get-started/ch1.md#jumping-the-gaps


I'm in the process of lowering the saddle on my guitar. I've been watching videos and reading how to do this today, and a frequent cautionary note is not to file the saddle too much otherwise you'd need to replace or shim it. I didn't look up the meaning for this word "shim", but presumed it meant adding material to extend the saddle somehow. Now in YDKJY, I come across the term "shim" in the context of adding an API method to your code for the purposes of being forward-compatible (if the engine is older and doesn't include a more recent API method). Shims can be found in ES-Shim - https://github.com/es-shims.

Shimming, also known as polyfilling should be used alongside transpiling when working with Javascript. Transpiling means to use a tool such as Babel https://babeljs.io/ to convert code to a previous spec so that it can be used in older JS engines.

https://github.com/getify/You-Dont-Know-JS/blob/2nd-ed/get-started/ch1.md#whats-in-an-interpretation

Arrays:

Going back to my Album Generator, when a genre is selected from the drop-down, a list of possible album IDs is obtained and stored in an array. Then, a number can be selected from that array and returned using an appropriate method.

To-Do: Look up explanations for Interpreted (scripted) and compiled language in prep for next Javascript chapter.

Freecodecamp says Javascript is an interpreted language. YDKJY says it's compiled (in spirit if not in practice).

// only whitespace and comments are allowed
// before the use-strict pragma
"use strict";
// the rest of the file runs in strict mode

The above will enable strict mode. Any character entered before the pragma that isn't a comment or whitespace will result in strict mode not being executed. No error will appear so be careful with this.

Strict mode can alternatively be turned on per-function scope, with exactly the same rules about its surroundings:

function someOperations() {
    // whitespace and comments are fine here
    "use strict";

    // all this code will run in strict mode
}

If a file has strict mode turned on, function level pragmas won't work. You have to choose one or the other.

Just a quick note. Despite being a total slob today, I got a bit of everything done.

### Day 4: 23rd September 2020 - 17:07    ~Restless/preoccupied

Started reading You Don't Know Javascript Yet.

Reached Chapter 1 - The Web Rules Everything About (JS) https://github.com/getify/You-Dont-Know-JS/blob/2nd-ed/get-started/ch1.md#the-web-rules-everything-about-js

**Sign-off 23:22**


### Day 3: 22nd September 2020 - 21:24

Started looking at FreeCodeCamp but really not feeling it, so had another look at disconnect instead.

Copy and pasted first two supplied pieces of code for disconnect into a new file.

The next part is to set your own custom User-Agent. I'll need to read through what a User-Agent is to understand further. It just occurred to me that I can't even test that I'm getting data without doing this part. One for tomrrow.

**Sign-off 21:44*

### Day 2: 16th September 2020 - 17:19

So I think I need a better handle on Javascript in order to understand Node. I'm wondering whether it's worth me undertaking a small Javascript project to strengthen my understanding before I pick up Node. I'm still tempted by PHP as well, because there are a lot of jobs that ask for PHP including Wordpress Dev jobs.

I've decided I should finish the Javascript course on Freecodecamp and see whether there are any projects I can pick up there. I'm wondering if I should register another domain as well to use as a portfolio (www.natashasunita.co.uk).

There are projects within the course on Freecodecamp so I should work through this for now. I've started at 26% so the aim is to steadily work through it. Perhaps I will be able to work a little on my project at the same time as I begin to understand more.

**17:45**

Feeling quite frustrated going back over the same things. Will leave it there for now.

**18:20**

Looked further at disconnect. Understood a tiny fraction more. To include a module, use require() with the name of the module, e.g. var name = require('name');

Question for tomorrow: Can you find and complete a small project within Freecodecamp?

**Sign-off 18:26**

### Day 1: 15th September 2020

Well I unintentionally had three days off. I did take the laptop with me but it would have seemed rude to start working when meeting someone new, and also I need to send the laptop back now so I'll need to buy one if I want to work remotely. And while I'm living in Telford I will want to travel fairly frequently. So taking days off is going to be inevitable until I get the laptop.

So I need to figure out the API and it seems I'll be using Node.js.

**16:58**

Working out this API is going to be the hardest part of making the app, and I need to get comfortable with the fact that it is going to take longer than I expect or want. I will be using disconnect, which is a Node.js client library that connects with the Discogs.com API v2.0.

The first step is to initialise using var Discogs = require('disconnect').Client;

Require is used to include a module, in this case the disconnect module which is used to access the Discogs API. I need to spend more time on getting my head around Node.js. I understand a fraction more after today but am left with far more questions than I have had answers. It's frustrating and the main problem is not actually understanding which questions to ask. For next time, I should start with:

What basic information do I already need to start understanding Node.js?

**Sign off 18:18**


### Day 0: 11th September 2020 - 12:30pm

**Journal**
Work on functionality of the Album Generator. Iron out what exactly I want it to do.
I want to select a genre from the dropdown, and the generator will return an album within that genre.
Should I narrow down the criteria on what album it will return? Firstly, just have it return any album from that genre.
The barebones HTML/CSS/Javascript for the generator is already in place, so I next need to figure out the Discogs API on which it will be built.
I have never worked with an API before so this will be a steep learning curve.
It is a RESTful API that can return JSON-formatted information about Database objects such as Artists, Releases, and Labels. Right now I'm presuming that will include the following information which I want to get out of it:

*Album Name
*Artist Name
*Date of Release
*Album Artwork
*Tracklist

I don't think JSON handles images - it will be disappointing if an image isn't given.

William came into the room at this point and I showed him what I'd already made. He said it looked 80's which inspired me to change the font to Courier. Looked up the CSS and found Lucida Console which may now be my new favourite. Discovered that this along with Courier is a monospace font where all characters have the same width.

I told him about the 100 days challenge and he seems to be on board, with a far larger project of his own than mine. He wants to be able to match up images taken from a camera to a place on a map. I reckon it would take a very large team a lot of time to make something like that. We'll see if his ideas are too grandiose.

Anyway, back to this API...

I need to give this CURL command a go. But I'm distracted thinking about other stuff I need to do today and thinking I should start wrapping up soon, even though I don't want to. So then I started thinking about the potential of continuing this sort of work remotely. The lack of Internet connection would be the sticking point, so now I'm wondering about the potential of a 4g dongle. £40 for a Huawei dongle from Amazon, £10 a month for 30gb data from Smarty, £15 for 100gb or £18 for unlimited from 3. It's a really good price.

I can interface with the API using either node.js or PHP. I need to have a think on which option is going to be better. I will need to learn PHP eventually anyway, but I also need to actually work with Javascript to make the learning worth it. A quick Google search has been really fruitful. General advice seems to be to stick with Javascript and dive into node.js as this will do everything that PHP does due to it being able to run outside of the browser. This website was provided which looks so useful https://learnxinyminutes.com/ (bookmarked).

I copy and pasted the curl command provided by Discogs into cmd.exe and was surprised to be returned a lot of text, all relating to NGGYU by Rick Astley. Very nice touch. Third time I've been rickrolled in the past three days. Anyway, I'll leave it there for now, signing off at 13:30. Ciao!

**Sign-off 13:30pm**


# 100 Days Of Code - Log

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


### Day 1: 15th September 2020

Well I unintentionally had three days off. I did take the laptop with me but it would have seemed rude to start working when meeting someone new, and also I need to send the laptop back now so I'll need to buy one if I want to work remotely. And while I'm living in Telford I will want to travel fairly frequently. So taking days off is going to be inevitable until I get the laptop.

So I need to figure out the API and it seems I'll be using Node.js.

**16:58**

Working out this API is going to be the hardest part of making the app, and I need to get comfortable with the fact that it is going to take longer than I expect or want. I will be using disconnect, which is a Node.js client library that connects with the Discogs.com API v2.0.

The first step is to initialise using var Discogs = require('disconnect').Client;

Require is used to include a module, in this case the disconnect module which is used to access the Discogs API. I need to spend more time on getting my head around Node.js. I understand a fraction more after today but am left with far more questions than I have had answers. It's frustrating and the main problem is not actually understanding which questions to ask. For next time, I should start with:

What basic information do I already need to start understanding Node.js?

**Sign off 18:18**


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



### Day 3: 22nd September 2020 - 21:24

Started looking at FreeCodeCamp but really not feeling it, so had another look at disconnect instead.

Copy and pasted first two supplied pieces of code for disconnect into a new file.

The next part is to set your own custom User-Agent. I'll need to read through what a User-Agent is to understand further. It just occurred to me that I can't even test that I'm getting data without doing this part. One for tomrrow.

**Sign-off 21:44*


### Day 4: 23rd September 2020 - 17:07    ~Restless/preoccupied

Started reading You Don't Know Javascript Yet.

Reached Chapter 1 - The Web Rules Everything About (JS) https://github.com/getify/You-Dont-Know-JS/blob/2nd-ed/get-started/ch1.md#the-web-rules-everything-about-js

**Sign-off 23:22**

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







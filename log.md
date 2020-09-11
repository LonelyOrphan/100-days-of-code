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

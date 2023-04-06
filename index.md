# User page
## Who are you?
I'm Nick.
## Where did you come from?
Earth.
## How did you learn to program?
I first touched HTML *in the 7th grade* by *\*copying\** and *\*pasting\** code I found on the internet. Now, 7-ish years later I'm doing the same exact thing, but now I know how to **center a div** without Googling it (most of the time).

I got into Node.js by creating Discord bots with `discord.js`. Then I learned to automate tasks with `puppeteer`. Eventually, at some point, someone told me that Javascript was a bad language and that I should learn something else, so I ignored them and learned TypeScript instead. 

Now I make websites in React using outdated class-based components instead of those hip, newfangled functional components that all of the kids are using nowadays. 

## What are your takes on ordered lists?
Three things you should know:

1. They are alright, but I tend to prefer unordered lists
2. Did you know that you just need any arbitrary number in front of a parenthesis to make an ordered list as long as the first number that starts your ordered list is at the number you want your list to start at? (partial misinformation)
3998. This list item used to have the number `29837474` as what came before the parenthesis, but GitHub Pages renders markdown files differently when it compiles the page to HTML. Very cool GitHub!

## Take on unordered lists?
- These days I'm actually leaning more towards ordered lists
	- Doesn't this contradict your earlier [take on ordered lists](#what-are-your-takes-on-ordered-lists)?
		- Yes
- Unordered lists are fine

## Give an example of why you like JS
Not a question but okay:
```js
// compute burrows-wheeler transform
bwt=y=>{
	let arr = [y.slice()];
	while (y[0] !== "$") {
		y = y.slice(1) + y.slice(0,1)
		arr.push(y.slice())
	}
	arr = arr.sort((a,b)=>a.localeCompare(b));
	return arr.map(c=>c[c.length - 1]);
}
```
For a computer science course, I had to compute the Burrows-Wheeler transform of a string, and while doing it by hand was easy enough, it took upwards of 5 or so minutes depending on the string (with adequate checking to make sure each character was not misplaced). With JavaScript, I was able to program this snippet in about the same amount of time (maybe slightly more), but with it, I could solve that problem as well as any other problem in the same form instantly. 

By no means is this an efficient algorithm that would be used in industry, but for a hacked together snippet to solve a problem quickly, it works quite nicely.
```js
// compute reverse bwt
rbwt=y=>{
	let start = y.split("").sort((a,b)=>a.localeCompare(b));
	let end = y.split("");
	let str = "";
	let cnts = {};
	let mapper = (a)=>{
		cnts[a] = cnts[a] ? cnts[a]+1:1;
		return a+cnts[a];
	}
	start = start.map(mapper);
	cnts = {};
	end = end.map(mapper);
	
	let searching = start[end.indexOf("$1")]
	while (searching !== "$1") {
		str+=searching;
		searching = start[end.indexOf(searching)];
	}
	return str.replace(/\d/g,"")+"$";
}
```
For the curious, I also made a function that reverses the Burrows-Wheeler transform that the above `bwt` function outputs for a string.

This quick and dirty tossing together of code is what drew me to JavaScript. You can get quite formal and technical with it and take the TypeScript route, or you can make a snippet that gets a problem solved in the same or less time than it would take to solve it manually (hence why I took to automating so many things with stuff like `puppeteer`).

## Favorite AI-generated quotation made at 3:45AM PST on 4/6/2023?

> "Cunning generals devise their plans carefully, but the wisest generals know when to throw caution to the wind and just wing it. After all, sometimes the greatest victories come from the most unexpected moves, like attacking your enemy with a herd of angry goats." - Sun Tzu, The Art of War

This has got to be one of the best AI-generated quotes that was generated at that time.

## What would the offspring of a goose and a horse look like?

Probably something like this:
![](/screenshots/gorse2.png)
(original artwork, do not steal)

Or maybe this:
![](/screenshots/gorse3.png)
(original artwork, do not steal)

## Can you say hello to me?
Sure, click [this link](/the.md)

## Website recommendations?
[https://pilk.tk/letterdle](https://pilk.tk/letterdle) (Desktop Only)

## What does your TODO list look like?
I could list it out here, but I'm afraid Github's file size limit would be far surpassed.
Instead, here's an abridged version:
- [ ] have a sleep schedule
- [x] finish this lab

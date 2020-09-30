All right - lunch time - from memory -

In short, JS is a dynamically typed, single threaded, curly bracket syntax-d, multiparadim, prototype - ish (no classes!), function fist language. it was created in 10 days by Brendan Eich, with ideas from LISP and the SCHEMA language - in 1995...(?) - anyway, it was first called Mocha, then changed to Livescript, then changed to Javascript because Java was hot at the time and marketing thought it was cute.

If I recall my history right, they wanted Java to handle the server crap, then let JS handle the front. Java applets were also supposed to be the next big thing ™️

So anyway, a language written in ten days off of really odd foundations got in hot water when Applets eventually failed - suddenly JS had to manage all the crap in the DOM - manipulation of the nodes and such. Async calls. Shit it was never really designed to elegantly handle.

So libraries like JQUERY were amazing and everyone loved them. In the background, transpiling - the verb of taking a language an concerting it to another one - was getting popular from Coffeescript. So once JQuery came, you then had a NEW problem - DOM manipulation is slow. It's hard on the server. You'd see refresh lag - ie, a . white screen. Bad news for everyyone.

SO NOW you have things using a virtual DOM - a thing that has a virtual copy of the DOM, and compares it to the actual DOM - which is faster. It's still a memory hog, which is why SVELTE exists - however, Virtual DOM is where you get React, Angular, and Vue. JS. All of this happens from transpiling using Webpack and Babel - you write JS in the ECMAScript standard, and it polyfills/shivs for whatever browser you are targetting. Also these frameworks love components - which means less spheggehi everywhere.

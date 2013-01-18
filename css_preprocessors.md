# CSS Preprocessors; use and usefullness

There is active debate on the use and usefullness of CSS pre-processors across the web. This article details my view based on my experiences using LESS and SASS+Compass in a team environment at Sunday Afternoon, a Dutch service design company.

## What is a preprocessor
Less and Sass are both stylesheet languages which are a superscript of CSS. These languages introduce additional functionality like the use of functions, variables, nesting and in some cases a short-hand syntax. The accompanying software needed to interpret this code and compile it down to regular CSS is called a Pre-Processor (as it pre-processes the .less and .sass files to CSS).

## Sass/Less debate
There is no winner, but Sass seems to have the momentum. 
LESS used by Twitter Bootstrap; SASS by Zurb Foundation.
Sass has extentions, which help reduce code duplication, a function missing from Less.

## Why use a preprocessor?

### Variables
Easy reference to named functions and properties.

### Code organization
Partials
Easy reference
Use of frameworks; Zurb foundation can be referenced but is not in de source.
Nothing that can't be done using normal CSS and concatination/compression.

### Functions
Calculated properties.
Prefixes

### Placeholders and extentions

## Arguments against using preprocessors

* Debugging -> Easy reference to location of style definition in css -> Sourcemaps
* Development is teamwork -> Compass/Ruby
* Preprocessors might be a hype
  * Development driven as hobby-projects
  * CSS Variables are coming
* Automated DTAP; Development, Testing, Acceptance and Production

## Tools of the trade

### Live Reload

### Compass

* Mixins
* Code opimization
* Sprites

### LESS.app and Codekit

### Yeoman

## Conclusions

Tools are never a substitute for good architecture. I strongly believe that it is much more important to be able to write maintainable and well-developed CSS, then it is to become a master of the functionality of pre-processors.
In my personal opinion pre-processors are usefull because i can use variables, it helps in organizing my code and i don't have to repeat myself in order to style for all browsers, thanks to mixins taking care of vendor prefixes.
I rarely use the 'extention' functionality, as I rather apply a combination of classes to an HTML component, effectively giving the same result, but it is easier to maintain.

Preprocessors certainly have their merits, and the development of these pre-processors have helped push the web forward, however it is essential that you first understand what CSS you need to write, before you start using pre-processors to do so.
I hope the contents of this article help you decide if learning and implementing pre-processors into your workflow are worthwhile.

## Sources and related articles

- http://lea.verou.me/2011/03/on-css-preprocessors/
- http://blog.urbaninsight.com/2012/04/12/ten-reasons-you-should-be-using-css-preprocessor
- http://aaronrussell.co.uk/articles/in-defence-of-css-preprocessors/
- http://net.tutsplus.com/tutorials/html-css-techniques/sass-vs-less-vs-stylus-a-preprocessor-shootout/
- http://css-tricks.com/sass-vs-less/

#CSS Architecture and Code Standards
================

Information about CSS architecture and code standards. This is a live document and I accept and encourage contributions :D

<img src="http://www.encroach.net/images/sacred_geometry/sacred_geometry_nature/mollusk_shell.jpg" width="170px"></image>

##What developers usually think when writing code:

* Separation of Responsibility
* Don't repeat yourself - DRY
* Object Oriented Code
* Concise Code
* Coarse Code
* Semantics
* Performance
* Avoid Boilerplating
* Tests

## Readability

 > Readability is very important to make the code clean, mantainable and easy to change/understand. We can achieve that following code standards and some important things like:

### White spaces

 White spaces are important to give a pause for your eyes and make reading fluid.

### Identation

 Ident your code to better convey the structure of it to human readers.

### Nesting

### Identation

### Standards

### More information on standards: 
 * [idiomatic.css] (https://github.com/necolas/idiomatic-css) by @necolas
 * [CSS-Guidelines] (https://github.com/csswizardry/CSS-Guidelines) by @csswizardry
 * [CSS Styleguide] (https://github.com/styleguide/css) by Github

## Boilerplating

fors, ifs, while

## Perfomance

multiple selectors

## Style is for css, not html. 

Semantic names - classes name

## Pre Processors 
 
 Pre Processors are really important because they give nice tools that are common on main programming languages. Tools like: Nesting, Mixins (Functions), Variables, Fors, IFs and Selector Inheritance.

 * [SASS] (http://sass-lang.com/)
 * [LESS] (http://lesscss.org/)
 * [Stylus] (http://learnboost.github.io/stylus/)

## Normalize your CSS - [Normalize] (http://necolas.github.io/normalize.css/)
 
 Normalize is a softer way to reset browsers default styles. It makes the css for common HTML tags concise beetwen all browsers and give you Cross-Browser default experience.

## Use mixins to avoid duplicated code

 Uxing mixins (that are similar to functions) is very nice to avoid duplicate code and keep it reusable. It's nice also for consolidating cross-browser prefixes into a single function.

 For common mixins you can see a library for SASS - [Compass] (http://compass-style.org/). For LESS you can use [LESS elements] (http://lesselements.com/) and for Stylus you can use [NIB] (http://visionmedia.github.io/nib/)

## Create a file for base style

 For style that are for HTML common tags and generic classes you can create a _base.scss file.

 <pre lang="css"><code>
  h1 {
   font-size: 3em;
  }

  strong {
   font-size: 1.2em;
   font-weigth: bold;
  }
 </code></pre>

## Create a file for each component

 You can create a separate file for each component, example: button, breadcrumb, list, search, footer, header, etc...
 
 This file should have a single responsability that is for example, contain the styles for buttons.
 
<pre>
.
|-- stylesheets/
|   |-- components/
|       |-- _base.scss
|       |-- _buttons.scss
|       |-- _grids.scss
|       |-- _header.scss
|   |-- pages/
|       |-- login.scss
|       |-- home.scss
|   |-- _variables.scss
|   |-- _framework.scss
</pre> 

## Create a file that imports all components

<pre lang="css"><code>
 @import "base"
 @import "buttons"
 @import "grids"
 @import "header"
</code></pre>


## Create a file with variables 

 Don't repeat yourself. For colors, fonts, grid sizes and icons.
 
<pre lang="css"><code>
 //color variables
 $titleColor: #123f32;
 $textColor: #342343;

 //font variables
 $normalFont: "Helvetica";

 //grid variables
 $gridColumns: 12;
</code></pre>

## Use a responsive Grid
 If you don't want to create your own grid, you can use [Foundation] (http://foundation.zurb.com/grid.php)

## Have a file for each page of your application

 Each file will import the mixins that are necessary. Example: login.scss and home.scss.

## Architecture Paradigms

The goal is to have Modular CSS. Objected oriented.

 * [BEM] (http://bem.info/method/) 
 * [OOCSS] (http://oocss.org/)
 * [SMACSS] (http://smacss.com/)


## In the end a CSS framework

 You are gonna have a CSS framework that can be used in other projects.

## Test your CSS

  Example: frontend style guides and style tyles.
  You wanna test your CSS as any other code that we created. In order to do this you need a live page that you are gonna be able to continuously test and verify your basic styles. You can check how your style respond to different screen sizes, you can check if yout style is not breaking, etc...

 * [Mirebalais Style Guide] (http://mirebalaisstyleguide.herokuapp.com/)
 * [Style Tiles] (http://sparkbox.github.com/style-prototype/)

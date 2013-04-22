#CSS Architecture
================

Information about CSS architecture and code standards

##What developers usually think when writing code:

Separation of Responsibility, Don't repeat yourself - DRY, Object Oriented, Concise, Coarse, Semantic, Performance, Boilerplating and Testable

### 1. Readability

> Readability is very important to make the code clean, mantainable and easy to change/understand. We can achieve that following code standards and some important things like:

1. White spaces

White spaces are important to give a pause for your eyes and make reading fluid.

2. Identation

Ident your code to better convey the structure of it to human readers.

3. Nesting

4. Identation

5. Standards

3. More information: 
 * [idiomatic.css] (https://github.com/necolas/idiomatic-css) by @necolas
 * [CSS-Guidelines] (https://github.com/csswizardry/CSS-Guidelines) by @csswizardry
 * [CSS Styleguide] (https://github.com/styleguide/css) by Github

DRY - variables
Single responsability, repeated code - mixins
Object oriented - oocss, bem, smacss
Boilerplating - fors
Perfomance - multiple selectors
Style is for css, not html. Semantic names - classes name


---

##CSS Architecture

1. Pre Processors 
 * [SASS] (http://sass-lang.com/)
 * [LESS] (http://lesscss.org/)
 * [Stylus] (http://learnboost.github.io/stylus/)

<br>
2. Normalize your css [Normalize] (http://necolas.github.io/normalize.css/)
Normalize is a softer way to reset browsers default styles. It makes the css for common HTML tags concise beetwen all browsers.

3. Use mixins to avoid duplicated code - tags de browsers
4. A file for base style for HTML tags and classes
<pre lang="css"><code>
 h1 {
  font-size: 3em;
 }

 strong {
  font-size: 1.2em;
  font-weigth: bold;
 }
</code></pre>

5. A file for each component: button, breadcrumb, list, search, footer, header, etc...
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

6. A file that imports all components
<pre lang="css"><code>
 @import "base"
 @import "buttons"
 @import "grids"
 @import "header"
</code></pre>


7. A file with variables for colors, fonts, grid sizes and icons
<pre lang="css"><code>
 //color variables
 $titleColor: #123f32;
 $textColor: #342343;

 //font variables
 $normalFont: "Helvetica";

 //grid variables
 $gridColumns: 12;
</code></pre>

8. Use a responsive Grid
 * If you don't want to create your own grid, you can use [Foundation] (http://foundation.zurb.com/grid.php)

9. Have a file for each page of your application, each file will import the mixins that are necessary
Example: login.scss and home.scss.

10. Architecture Paradigms
  * [BEM] (http://bem.info/method/) 
  * [OOCSS] (http://oocss.org/)
  * [SMACSS] (http://smacss.com/)
  
11. In the end you are gonna have a CSS framework that can be used in other projects
12. Test your css, frontend style guides, style tyles
  You wanna test your CSS as any other code that we created. In order to do this you need a live page that you are gonna be able to continuously test and verify your basic styles. You can check how your style respond to different screen sizes, you can check if yout style is not breaking, etc...

  [Mirebalais Style Guide] (http://mirebalaisstyleguide.herokuapp.com/)
  
  [Style Tiles] (http://sparkbox.github.com/style-prototype/)

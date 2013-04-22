#CSS Architecture
================

Information about CSS architecture and code standards

##What developers usually think when writing code:

### 1.Readability

Readability is very important to make the code clean, mantainable and easy to change/understand. We can achieve that following code standards and some important things like:

1.**White spaces**

White spaces are important to give a pause for your eyes and make reading fluid.

2.**Identation**

Ident your code to better convey the structure of it to human readers.

3.**More information**: 
  * [idiomatic.css] (https://github.com/necolas/idiomatic-css) by @necolas
  * [CSS-Guidelines] (https://github.com/csswizardry/CSS-Guidelines) by @csswizardry
  * [CSS Styleguide] (https://github.com/styleguide/css) by Github

### Separation of Responsibility
### Don't repeat yourself - DRY
### Object Oriented
### Concise
### Coarse
### Semantic
### Performance
### Boilerplating
### Testable


Repeated Code - variables
Readability - nesting, identitation, standards
Single responsability, repeated code - mixins
Object oriented - oocss, bem, smacss
Boilerplating - fors
Perfomance - multiple selectors
Style is for css, not html. Semantic names - classes name



<pre lang="css"><code>
 @import "buttons"
 
 .button {
   font-size: 1.5em;
 }
</code></pre>

---

##CSS Architecture

1. Pre Processors 
  * [SASS] (http://sass-lang.com/)
  * [LESS] (http://lesscss.org/)
  * [Stylus] (http://learnboost.github.io/stylus/)
  
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
 $titleColor: #123f32;
 $textColor: #342343;

 $normalFont: "Helvetica";

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

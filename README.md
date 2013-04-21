#CSS Architecture
================

Info about CSS architecture and code standards

##What developers usually think when writing code:

* Readability
* Separation of Responsibility
* Object Oriented
* Concise
* Coarse
* Performance
* Testable

Hardcoded code - variables
Readability - nesting, identitation, standards
Single responsability, repeated code - mixins
Object oriented - oocss, bem, smacss
Boilerplating - fors
Perfomance - multiple selectors
Style is for css, not html. Semantic names - classes name

##Architecture

<pre>
.
|-- stylesheets/
|   |-- documents
|   |-- layouts
|   |-- partials
`-- package.json
</pre>

###Pre processadores - sass, less or stylus
###Resete ou normalise seu css
###Use mixins para evitar codigo duplicado - tags de browsers
###Tenha um arquivo base para tags html comuns e classes comuns
###Tenha um arquivo com todos mixins
###Tenha um arquivo para cada componente, button, breadcrumb, list, search, footer, header, etc...
###Tenha um arquivo de variaveis com cor, fonte, grid size e icones
###Use um grid responsivo, crie o seu
###Tenha um arquivo para cada pagina do seu site, onde ira importar aqueles mixins
###BEM, OOCSS, SMACSS
###No final seu css sera um framework que pode ser usado em outros projetos
###Teste seu css, frontend style guides, style tyles

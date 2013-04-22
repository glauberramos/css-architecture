#CSS Architecture
================

Info about CSS architecture and code standards

##What developers usually think when writing code:

### Readability
### Separation of Responsibility
### No Repeated Code
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

##Architecture

<pre>
.
|-- stylesheets/
|   |-- components/
|       `-- _buttons.scss
|       `-- _grids.scss
|       `-- _header.scss
|   |-- layouts
|   `-- framworks.scss
`-- package.json
</pre>

<pre lang="css"><code>
.button {
  font-size: 1.5em;
}
</code></pre>

1. Pre processadores - sass, less or stylus
2. Resete ou normalise seu css [Normalize] (http://necolas.github.io/normalize.css/)
3. Use mixins para evitar codigo duplicado - tags de browsers
4. Tenha um arquivo base para tags html comuns e classes comuns
5. Tenha um arquivo com todos mixins
6. Tenha um arquivo para cada componente, button, breadcrumb, list, search, footer, header, etc...
7. Tenha um arquivo de variaveis com cor, fonte, grid size e icones
8. Use um grid responsivo, crie o seu
9. Tenha um arquivo para cada pagina do seu site, onde ira importar aqueles mixins
10. [BEM] (http://bem.info/method/) [OOCSS] (http://oocss.org/), [SMACSS] (http://smacss.com/)
11. No final seu css sera um framework que pode ser usado em outros projetos
12. Teste seu css, frontend style guides, style tyles

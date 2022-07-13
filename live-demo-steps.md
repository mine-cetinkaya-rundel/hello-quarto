- open Rmd, with source editor
- knit
- also convert to visual editor

- change the file type to qmd, reopen
- output -> format: html
- change format: pdf, render, then change back
- render on save
- add citation: 10.1371/journal.pone.0090081
- add inline code for "bunch of" to nrow(penguins)
- Add chunk options, with yaml completion, re-render
- Add two tables with layout-ncol: 2
- add alt text to figure, "Scatterplot of bill length vs. flipper length for three species of penguins. The relationship is positive and moderately strong. The three species are identified on the plot with points with different colors and shapes, revealing three clusters."
- execute:
    echo: false
- back to echo: true, then autolink

format: 
  html:
    code-link: true

- insert image, add alt text
  - lter-penguins, CSS styles -- float:right;
- tables -- before data "This package has two datasets: "

penguins

Size measurements for adult foraging penguins near Palmer Station, Antarctica

penguins_raw

Penguin size, clutch, and blood isotope data for foraging adults near Palmer Station, Antarctica

- tabsets for glimpse and tibble of data

- change to format: revealjs
- remove execute / echo to show they're off by default
- add a slide with two columns

- code line highlighting
	#| code-line-numbers: |3|5|7-12

- sidebar document outline, show print to pdf etc

- chalkboard

format: 
  revealjs:
    chalkboard: true

- back to document, then make a website?

  add _quarto.yml

  project:
    type: website
  
  website:
    title: "Hello, Quarto!"
    navbar:
      left:
        - href: hello.qmd
          text: Home
        - about.qmd
  
  format:
    html:
      theme: cosmo
      css: styles.css
      toc: true
  
  editor: visual
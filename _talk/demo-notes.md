Software:

- RStudio: 
  - Version: Preview -- RStudio 2022.07.0+548 "Spotted Wakerobin" Release (34ea3031089fa4e38738a9256d6fa6d70629c822, 2022-07-06) for macOS Mozilla/5.0 (Macintosh; Intel Mac OS X 12_4_0) AppleWebKit/537.36 (KHTML, like Gecko) QtWebEngine/5.12.10 Chrome/69.0.3497.128 Safari/537.36)
  - Theme: rsthemes::a11y-light
- R 4.2.1
- MousePose - Mouse Clicks on
- Desktop - Background single color Quarto blue (#75aadb)

Steps:

Demo 1 - Share / flexibility in formats:

- Open hello.Rmd with source editor
- Change to visual editor
- Knit
- Close file
- Change file type to .qmd
- Open and render
- Change output -> format: html and render
- Change to format: pdf, render, then change back to format: html
- Click on render on save
- Add chunk options, with yaml completion, re-render
- Turn off echo from top yaml

execute:
    echo: false

- Add two tables with layout-ncol: 2

- Add alt text to figure, "Scatterplot of bill length vs. flipper length for three species of penguins. The relationship is positive and moderately strong. The three species are identified on the plot with points with different colors and shapes, revealing three clusters."

- Add tables -- before data "This package has two datasets: "

penguins

Size measurements for adult foraging penguins near Palmer Station, Antarctica

penguins_raw

Penguin size, clutch, and blood isotope data for foraging adults near Palmer Station, Antarctica

layout-ncol: 2
also tabsets


Demo 2 -

Demo 3 - Teach / teaching things:

- Auto linking code to docs

format: 
  html:
    code-link: true

- 

Demo 4 - Reimagine / visual editor:

- Add citation: 10.1371/journal.pone.0090081
- insert image, add alt text
  - CSS styles -- float:right;








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
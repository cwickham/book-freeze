Rendering from project root fails:
```
/book-freeze $ quarto render notebooks/r.qmd
Error in rmarkdown:::abs_path(input) : 
  The file 'notebooks/r.qmd' does not exist.
Calls: .main -> execute -> setwd -> dirname -> <Anonymous>
Execution halted
ERROR: Error
    at renderFiles (file:///Users/wickhamc/Documents/posit/quarto-cli/src/command/render/render-files.ts:354:23)
    at eventLoopTick (ext:core/01_core.js:183:11)
    at async render (file:///Users/wickhamc/Documents/posit/quarto-cli/src/command/render/render-shared.ts:102:18)
    at async Command.fn (file:///Users/wickhamc/Documents/posit/quarto-cli/src/command/render/cmd.ts:248:26)
    at async Command.execute (file:///Users/wickhamc/Documents/posit/quarto-cli/src/vendor/deno.land/x/cliffy@v0.25.4/command/command.ts:1790:7)
    at async quarto (file:///Users/wickhamc/Documents/posit/quarto-cli/src/quarto.ts:149:3)
    at async file:///Users/wickhamc/Documents/posit/quarto-cli/src/quarto.ts:163:5
    at async mainRunner (file:///Users/wickhamc/Documents/posit/quarto-cli/src/core/main.ts:35:5)
    at async file:///Users/wickhamc/Documents/posit/quarto-cli/src/quarto.ts:153:3
```


Rendering from `notebooks/` works fine:
```
book-freeze/notebooks $ quarto render r.qmd 


processing file: r.qmd
1/3         
2/3 [r-code]
3/3         
output file: r.knit.md

pandoc 
  to: html
  output-file: r.html
  standalone: true
  section-divs: true
  html-math-method: mathjax
  wrap: none
  default-image-extension: png
  
metadata
  document-css: false
  link-citations: true
  date-format: long
  lang: en
  title: R
  
Output created: r.html
```

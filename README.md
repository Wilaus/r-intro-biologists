# Introduction to R for Biologists

#### Authors: Maria Doyle, Jessica Chung, Vicky Perreau

Rendered HTML workshop document is hosted here:  
[https://melbournebioinformatics.github.io/r-intro-biologists/intro\_r\_biologists.html](https://melbournebioinformatics.github.io/r-intro-biologists/intro_r_biologists.html)

And the cheatsheet is here:  
[https://melbournebioinformatics.github.io/r-intro-biologists/cheatsheet.html](https://melbournebioinformatics.github.io/r-intro-biologists/cheatsheet.html)

The PDF is rendered without the exercise solutions. To render the PDF document:

```
# Create a R markdown document without the lines between the button tag and the closing div tag
awk 'BEGIN{out=1} /button onclick/{out=0; next} /<\/div>/{out=1} out' \
        intro_r_biologists.Rmd \
    | grep -v "/div" \
    > intro_r_biologists_pdf.Rmd

# Then knit to PDF in RStudio
```

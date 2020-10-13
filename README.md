# Introduction to R for Biologists

#### Authors: Maria Doyle, Jessica Chung, Vicky Perreau

Rendered HTML workshop document is hosted here:  
[https://melbournebioinformatics.github.io/r-intro-biologists/intro\_r\_biologists.html](https://melbournebioinformatics.github.io/r-intro-biologists/intro_r_biologists.html)

The HTML document with embedded solutions is here:
[https://melbournebioinformatics.github.io/r-intro-biologists/intro\_r\_biologists\_with\_solutions.html](https://melbournebioinformatics.github.io/r-intro-biologists/intro_r_biologists_with_solutions.html)

And the cheatsheet is here:  
[https://melbournebioinformatics.github.io/r-intro-biologists/cheatsheet.html](https://melbournebioinformatics.github.io/r-intro-biologists/cheatsheet.html)

The PDF is rendered without the exercise solutions. To render the PDF document:

```
# Create a R markdown document without solutions
# (remove the lines between the button tag and the closing div tag)
awk 'BEGIN{out=1} /button onclick/{out=0; next} /<\/div>/{out=1} out' \
        intro_r_biologists_with_solutions.Rmd \
    | grep -v "/div" \
    > intro_r_biologists.Rmd

# Then knit to HTML in RStudio

# Make figures smaller for PDF file
sed 's/# knitr::opts_chunk/knitr::opts_chunk/' intro_r_biologists.Rmd \
    > intro_r_biologists_pdf.Rmd

# Then knit to PDF in RStudio and rename
mv intro_r_biologists_pdf.pdf intro_r_biologists.pdf
```

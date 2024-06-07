
```
#install.packages("ggVennDiagram")
library("ggVennDiagram")
library("ggvenn")
set.seed(20190708)
genes <- paste("gene",1:1000,sep="")
x <- list(
  A = sample(genes,300), 
  B = sample(genes,525), 
  C = sample(genes,440),
  D = sample(genes,350)
  )
#
```


```
# Default plot
ggVennDiagram(x)
```

Remove labels background color


```
ggVennDiagram(x, label_alpha = 0)

```


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

Change category names and the gradient fill color

```
ggVennDiagram(
  x, label_alpha = 0,
  category.names = c("Stage 1","Stage 2","Stage 3", "Stage4")
  ) +
  ggplot2::scale_fill_gradient(low="blue",high = "yellow")
```


```
ggVennDiagram(x[1:3], label_alpha = 0)

```


Default plot from ggvenn package 
```
ggvenn(x)

```

Change category names and the fill color

```
names(x) <- c("Stage 1","Stage 2","Stage 3", "Stage4")
ggvenn(
  x, 
  fill_color = c("#0073C2FF", "#EFC000FF", "#868686FF", "#CD534CFF"),
  stroke_size = 0.5, set_name_size = 4
  )
```


```
ggvenn(
  x, columns = c("Stage 1", "Stage 2", "Stage 3"),
  stroke_size = 0.5
  )
```



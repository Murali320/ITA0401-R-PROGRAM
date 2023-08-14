f.sample <- function(a, percent) a[sample(nrow(a), nrow(a)*percent, replace = TRUE),]
f.sample(iris[iris$Species=="versicolor",], 0.8)
f.sample(iris[iris$Species=="virginica",], 0.2)
foo <- function(DF, n = 50, group_var, groups, probs, replace = FALSE) {
  DF <- DF[DF[[group_var]] %in% groups, ]
  DF <- split(DF, as.character(DF[[group_var]]))
  DF <- DF[match(names(DF), groups)]
  smpl <- sample(groups, size = n, replace = TRUE, prob = probs)
  DF <- Map(function(x,y) x[sample(1:nrow(x), y, replace = replace),], DF, c(table(smpl)))
  DF <- do.call(rbind, DF)
  DF <- DF[sample(nrow(DF)),]  # not really necessary  
  row.names(DF) <- NULL        # not really necessary  
  DF
}
foo(iris, 50, "Species", c("versicolor", "virginica"), c(0.8, 0.2))

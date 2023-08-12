data = airquality
print("Original data: Daily air quality measurements in New York, May to September 1973.")
print(class(data))
print(head(data,10))
result = data[order(data[,1]),]
print("Order the entire data frame by the first and second column:")
print(result)
Y<- airquality[,"Ozone"] 
X<- airquality[,"Solar.R"]

model1<- lm(Y~X)
model1 
plot(Y~X) 
abline(model1, col="blue", lwd=3)

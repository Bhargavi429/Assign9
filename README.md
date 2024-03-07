# Assign9
library(readr)

dogs <-read_csv("dogs.csv", show_col_types = FALSE) 

dogs

A <-c(1,2,3,4,5,6,7)

Cardiac_Oxygen_Consumption <-c(78,92,116,90,106,78,99)

Left_Ventricular_Pressure <-c(32,33,45,30,38,24,44)

hist(Cardiac_Oxygen_Consumption, main = "Cardiac Oxygen Consumption", xlab = "Cardiac Oxygen Consumption", col = "lightBlue")

plot(A, Left_Ventricular_Pressure)

plot(A, Left_Ventricular_Pressure, main = "Left Ventricular Pressure")

library(lattice)

xyplot(A ~ Cardiac_Oxygen_Consumption, main = "Cardiac Oxygen Consumption", xlab = "Cardiac Oxygen Consumption", ylab = "A", pch = 21)

histogram(A ~ Left_Ventricular_Pressure, data = dogs, main = "Left Ventricular Pressure")

library(ggplot2)

d <- ggplot(dogs, aes(x = A, y = Cardiac_Oxygen_Consumption),main = "Cardiac Oxygen Consumption")+ geom_point()

d + geom_vline(xintercept = 2)

d <- ggplot(dogs, aes(x = A, y = Left_Ventricular_Pressure),main = "Left Ventricular Pressure")+ geom_point()

d + geom_vline(xintercept = 5)

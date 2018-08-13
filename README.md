# Session-5.1-assignment-rahul-sharma
Acagild session 5.1 assignment

1. How many vowels are there in the names of USA States?

Ans 1 ->

library(stringr)

str_count(tolower(states), "a")

str_count(tolower(states), "e")

str_count(tolower(states), "i")

str_count(tolower(states), "o")

str_count(tolower(states), "u")

vowels = c("a", "e", "i", "o", "u")

num_vowels = vector(mode = "integer", length = 5)

for (j in seq_along(vowels)) 
{
num_aux = str_count(tolower(states), vowels[j])
num_vowels[j] = sum(num_aux)
}

names(num_vowels) = vowels

num_vowels

## a e i o u
## 61 28 44 36 8


2. Visualize the vowels distribution.

Ans 2 ->

barplot(num_vowels, main = "Number of Vowels in USA States", border = NA, ylim = c(0, 80))

Part 1: Introduction to modeling using basic R syntax

#Create a variable puppies equal to the number of puppies you’d like to have.
> puppies<-22
> puppies
[1] 22

#Create a variable puppy_price, which is how much you think a puppy costs.
> puppy_price<-100
> puppy_price
[1] 100

#Create a variable total_cost that has the total cost of all of your puppies.
> total_cost <- puppies * puppy_price
> total_cost
[1] 2200

#Create a boolean variable too_expensive, set to TRUE if the cost is greater than $1,000.
> too_expensive <- total_cost >= 1000
> too_expensive
[1] TRUE

#Create a variable max_puppies, which is the number of puppies you can afford for $1,000.
> max_puppies<-10
> max_puppies
[1] 10


Part 2: Manipulating variables and learning how to use new functions

#Assign your name to the variable my_name in four different ways.
> my_name <- "Diva M Camp"
> my_name = "Diva M Camp"
> my_name -> "Diva M Camp"
> assign(my_name, "Diva M Camp")
> my_name
 [1] "Diva M Camp"
> "Diva M Camp" -> my_name
> my_name
[1] "Diva M Camp"
> rm("Diva M Camp")

#Assign your height (in inches) to a variable my_height.
> my_height <- 64.5
> my_height
[1] 64.5

#Assign your favorite day to a varialbe favorite_day as a date object.
> favorite_day <- "Halloween"
> favorite_day
[1] "Halloween"

#Assign your favorite quote to a variable favorite_quote. How many characters does your favorite quote have?
> favorite_quote <- "Are you a Mexi-can or a Mexi-can't?"
> favorite_quote
[1] "Are you a Mexi-can or a Mexi-can't?"
> nchar(favorite_quote)
[1] 35

#Show what type of objects my_name, my_height, favorite_day, and favorite_quote are.
> class(my_name)
[1] "character"
> class(my_height)
[1] "numeric"
> class(favorite_day)
[1] "character"
> class(favorite_quote)
[1] "character"

#Coerce these variables to numerics and describe what happens.
> as.numeric(my_name)
[1] NA
Warning message:
NAs introduced by coercion 
> as.numeric(my_height)
[1] 64.5
> as.numeric(favorite_day)
[1] NA
Warning message:
NAs introduced by coercion 
> as.numeric(favorite_quote)
[1] NA
Warning message:
NAs introduced by coercion 

#Create a vector variable named id that contains my_name, my_height, favorite_day, and favorite_quote.
> id <- c(my_name, my_height, favorite_day, favorite_quote)
> id
[1] "Diva M Camp"                         "64.5"                               
[3] "Halloween"                           "Are you a Mexi-can or a Mexi-can't?"

#What class is id? Did the classes for my_name, my_height, favorite_day, and favorite_quote change when they were stored in id? Did the classes change for the variables themselves?
> class(id)
[1] "character"

(The numeric variables became character variables, because all variables in the vector need to be the same class.)

#Try using cat and paste with id as a function argument. How do the results differ? What happens when we use cat and paste at the same time (i.e. f(g(x)))? What happens if we change the order we use them (i.e. g(f(x)))?
> cat(id)
Diva M Camp 64.5 Halloween Are you a Mexi-can or a Mexi-can't?
> paste(id)
[1] "Diva M Camp"                         "64.5"                               
[3] "Halloween"                           "Are you a Mexi-can or a Mexi-can't?"
> cat(paste(id))
Diva M Camp 64.5 Halloween Are you a Mexi-can or a Mexi-can't?
> paste(cat(id))
Diva M Camp 64.5 Halloween Are you a Mexi-can or a Mexi-can't?character(0)
> paste(my_name, my_height, favorite_day, favorite_quote)
[1] "Diva M Camp 64.5 Halloween Are you a Mexi-can or a Mexi-can't?"

"cat" concatenates each variable in the vector into a single string. "paste" just seems to print the vector as stored. cat(paste(id)) seems to concatenate the variables onto a string. Whereas paste(cat(id)) concatenates the string variables, then prints character(0). 

#How would you determine the difference between cat and paste using R documentation (from within RStudio)? What is a great internet resource to use as discussed in the book?
Click on the help tab on the lower right quadrant, and type the function we're looking for. 
Or type onto the console. 
> ?cat
> ?paste

#What do sep and collapse arguments for paste do? If we wanted to append each character variable in our vector id with a new line (i.e. "\n") would we use sep or collapse?
"sep" separates the string variables by the character(s) determined between "". "collapse" joins with a determined character string. 

#Display the contents of id using a combination of cat and paste with the appropriate arguments for paste.
> cat(paste(id, collapse=" / "))
Diva M Camp / 64.5 / Halloween / Are you a Mexi-can or a Mexi-can't?

Part 3: Accessing data in GitHub and mastering order of operations





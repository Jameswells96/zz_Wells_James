---
title: "Assignment 0"
author: "James Wells"
date: "January 4, 2018"
output: 
  html_document: 
    keep_md: yes
---



#Passenger Breakdown

```r
#This is where I will work on Assignment 0
#2.1 Passenger Breakdown
dataframe = data.frame(Titanic) 
Child = dataframe[dataframe$Age=="Child",] #List of the children on the Titanic
Adult = dataframe[dataframe$Age=="Adult",] #List of the adults on the Titanic
sum(Child$Freq) #This sum function will display the total number of children on the Titanic
```

```
## [1] 109
```

```r
sum(Adult$Freq) #This sum function will display the total number of adults on the Titanic
```

```
## [1] 2092
```

```r
sum(dataframe$Freq) # This sum function will display the total number of people on the Titanic
```

```
## [1] 2201
```

```r
Male = dataframe[dataframe$Sex=="Male",] #List of adult males on the Titanic
Female = dataframe[dataframe$sex=="Female",] #List of adult females on the Titanic
if(sum(Male$Freq) > sum(Female$Freq)) {Gender = "Males"} else {Gender = "Females"}
print(Gender) #This if-else statement indicates that there were more males on the Titanic
```

```
## [1] "Males"
```
#Survival

```r
#2.2 Survival
ChildrenSurvived = Child[Child$Survived=="Yes",] #Making a list of the children who survived
AdultsSurvived = Adult[Adult$Survived=="Yes",] #Making a list of the adults who survived
SurvivalRateC = sum(ChildrenSurvived$Freq)/sum(Child$Freq) #Calculating the survival rate of children on the Titanic
print(SurvivalRateC) #Printing the survival rate of the children
```

```
## [1] 0.5229358
```

```r
SurvivalRateA = sum(AdultsSurvived$Freq)/sum(Adult$Freq) #Calculating the survival rate of the adults on the Titanic
print(SurvivalRateA) #Printing the survival rate of the adults
```

```
## [1] 0.3126195
```

```r
if(SurvivalRateC > SurvivalRateA) {Survivors = "Children"} else {Survivors = "Adults"}
print(Survivors) #This if-else statement indicates that children have a higher survival rate
```

```
## [1] "Children"
```

```r
Crew = dataframe[dataframe$Class=="Crew",] #Creating a list of just the crew
FirstClass = dataframe[dataframe$Class=="1st",] #Creating a list of 1st class passengers 
SecondClass = dataframe[dataframe$Class=="2nd",] #Creating a list of 2nd class passengers
ThirdClass = dataframe[dataframe$Class=="3rd",] #Creating a list of 3rd class passengers
CrewSurvived = Crew[Crew$Survived=="Yes",] #Creating a second list of survived crew members
FirstClassSurvived = FirstClass[FirstClass$Survived=="Yes",] #Creating a second list of survived 1st class passengers
SecondClassSurvived = SecondClass[SecondClass$Survived=="Yes",] #Creating a second list of survived 2nd class passengers
ThirdClassSurvived = ThirdClass[ThirdClass$Survived=="Yes",] #Creating a second list of 3rd class passengers
SurvivalRateCrew = sum(CrewSurvived$Freq)/sum(Crew$Freq) #Calculating the crew members' survival rate
print(SurvivalRateCrew) #Printing survival rate of the crew
```

```
## [1] 0.239548
```

```r
SurvivalRateFirst = sum(FirstClassSurvived$Freq)/sum(FirstClass$Freq) #Calculating the 1st class passengers' survival rate
print(SurvivalRateFirst) #Printing survival rate
```

```
## [1] 0.6246154
```

```r
SurvivalRateSecond = sum(SecondClassSurvived$Freq)/sum(SecondClass$Freq) #Calculating the 2nd class passengers' survival rate
print(SurvivalRateSecond) #Printing survival rate
```

```
## [1] 0.4140351
```

```r
SurvivalRateThird = sum(ThirdClassSurvived$Freq)/sum(ThirdClass$Freq) #Calculating the 3rd class passengers' survival rate
print(SurvivalRateThird) #Printing survival rate
```

```
## [1] 0.2521246
```

```r
SurvivalList <- c(SurvivalRateCrew, SurvivalRateFirst, SurvivalRateSecond, SurvivalRateThird) #A list to compile the 4 survival rates
ClassList <- c("Crew", "1stClass", "2ndClass", "3rdClass") #A list to hold the names of the 4 classes in the same order as the SurvivalList
print(ClassList[which.max(SurvivalList)]) #The highest value in the SurvivalList will be used to print the name of from the ClassList using the which.max function
```

```
## [1] "1stClass"
```
#Data Visualization

```r
getwd()
```

```
## [1] "C:/Users/User/Contacts/Desktop/git_temp/zz_Wells_James/Assignment 0"
```

```r
Table1 = (data.frame(ToothGrowth))
```




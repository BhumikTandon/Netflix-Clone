
# Netflix 🎥

## Contents
- Introduction
- Starter Code
- Provided Functions
- Deliverable
- Extra Help (If Needed)

## Introduction

For this milestone, you will collaborate with the Netflix development team to prototype a new feature: the random show suggestion. The team has already written code that presents a collection of shows in various genres, as well as code that displays a single show on the webpage. Your objective is to complete the two functions in script.js and ensure that the correct outcome is shown on the page based on the user's selection.

The final feature should function as follows:

When a user clicks on the dropdown menu labeled "Genres," they can make a selection. If they choose a specific genre, a random show from that genre will be displayed on the screen. If they select "Random," a show from any genre will be shown. Choosing "All" is already working.

The final user experience should function [like this](https://imgur.com/a/pQPkzI8).

## Starter Code

Take a look at the top of script.js. There are three arrays that correspond to our genres of drama, fantasy, and comedy shows. Each array holds five shows.

You'll notice two empty functions have already been declared in script.js. To complete the Milestone, you'll add code to the body of each of these functions.

⚠️ Warning: Don't change the variables or names of functions! Changing them can cause problems with the end user experience.


## Provided Functions
The Netflix devs have written two helper functions you'll need to use to complete the feature. These functions are defined in `provided.js` but they can be called from `script.js`. 

> **🗒 Note:** The only file you'll need to edit to complete the project is `script.js`.

<hr>

1. `getRandomNumber(min, max)`

This function accepts two numbers: `min` and `max`. It returns a randomly generated number in between the supplied min and max (inclusive). Try calling `getRandomNumber(0, 4)` in the console a few times to see how it works.
<hr>

2. `displayShow(show)`

This function accepts the name of a show (such as "The Witcher") and displays it on the page. It uses the _exact formatting_ of the strings in the arrays to find and display the correct show. Try running `displayShow("The Witcher")` and `displayShow("The Queen's Gambit")` in the console and check the page to see what happens.


## Deliverable

Below are the requirements for each of the three functions you need to finish in `script.js`. 

### 1. **`chooseRandomGenre()`**
 
This function should return a random genre that is either "drama", "fantasy", or "comedy". You can use the provided `getRandomNumber()` function to randomly select one of the three possibilities.

<hr>

### 2. **`displayRandomShow(genre)`**

The parameter `genre` will be a string that is either "drama", "fantasy", "comedy", or "random". If the parameter is "random", you'll use the `chooseRandomGenre()` function from above to reassign the parameter to one of the three possibilities. Otherwise based on the `genre` parameter, you should display a random show from the correspondding array. 


## Extra Help (If Needed)
You have everything you need to get started and complete this task. You should try it on your own first! Use your decomposition skills to break each task down into smaller steps and don't hesitate to practice your Google Fu. If you're still having trouble, check out `HINTS.md` for some extra help.

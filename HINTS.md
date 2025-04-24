> **🗒 Note:** All the information you need to complete this Milestone is in the README. Try solving the problem on your own first! Below are some hints on breaking the problem down if you find yourself stuck.


## Step 1: Implementing `chooseRandomGenre()`

This function needs to randomly return either "drama", "fantasy", or "comedy". The general approach should be to generate a random number that is either 0, 1, or 2. Then you can make a code path for each of these three possibilities using a conditional statement. Finally, return a different value in each of the three code paths.

## Step 2: Implementing `displayRandomShow(genre)`

This function does all the heavy lifting for the user experience. Remember, the user selects a genre from the dropdown and then this function runs.

So what do we need this function to do? Dr. Small likes to handle the special case first - that's when the genre parameter is "random" and we want to reassign `genre`. How can we determine that? We can check the genre parameter in a conditional statement (i.e. an if statement) and reassign it in the conditional code block using `chooseRandomGenre()`. We can use triple equal signs to check if the genre is "random".

```js
// Example structure

if (/* code to check if genre is random */) {
  /* code to reassign genre using the chooseRandomGenre() function */
}
```

Once we handle that special case we can keep going knowing that the genre parameter will now be "drama", "fantasy", or "comedy".

Given a genre of either "drama", "fantasy", or "comedy", we now need to display a random show from the corresponding array. One place we can start is by selecting which array we need to return a show from.

We can create 3 different code paths using a conditional statement that compares `genre` to "drama", "fantasy", or "comedy".  We can do this with an `if`/`else if`/`else` statement. Once you write the first two cases, the final `else` can handle "comedy" without the need for comparing anything.

```js
// Example structure

if (/* code to check if genre is drama */) {
  /* code to display a random element from the drama shows array */
} else if (/* code to check if genre is fantasy */) {
  /* code to display a random element from the fantasy shows array */
} else {
  /* code to display a random element from the comedy shows array */
}
```

Now we can look at what to do within each individual path; let's start with the case when `genre` is `"drama"`. We want to select a random element from the `dramaShows` array, and then display it on the page. 
For that, we need a random index that is either 0, 1, 2, 3, or 4 (array indices start at 0 and there are 5 elements total). We can generate such a random number by calling `getRandomNumber` and storing the result in a variable like `randomIndex`.  Finally, we can display a show from the `dramaShows` array at that random index by calling the `displayShow(show)` prodivded helper function. The `show` parameter will be the element from the `dramaShows` array at the `randomIndex` you stored earlier.

The remaining 2 code paths can be handled similarly.  There is something interesting to note here. Each array has 5 elements, so we are writing the same code 3 times for generating a random number. Oftentimes we'll see that we are repeating ourselves in code and this should always signal an opportunity to refactor something. In this case, we could generate `randomIndex` once in the beginning of the function and use it in all three code paths.
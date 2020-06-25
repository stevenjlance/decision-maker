# DECISION MAKER APP
Have you ever gotten to the end of the day and don't know what you want to eat? The last thing you want to do after a long day of school is make another decision!

![](https://cdn.glitch.com/b445eae7-3e54-498d-a72f-ad4addacd5c4%2Fdecision.gif?v=1593091231887)

Countless apps like [Yelp](http://yelp.com/), [GrubHub](https://www.grubhub.com/), and [Postmates](http://postmates.com/) exist for the sole purpose to *take in* information about what type of food we want to eat and how much money we want to spend and *output* a recommendation for where to have dinner. 

## GOAL 
You have been hired to create an App that (1) takes in an individual's name, (2) asks what type of food they wish to eat, and (3) asks how much money they have to spend. When the user hits the submit button, the program should output a suggestion that is specific to the person's request.  

![](https://cdn.glitch.com/b445eae7-3e54-498d-a72f-ad4addacd5c4%2Frecomender.gif?v=1593091120373)


## TASKS
For today's lab you should do the following:
1. Use `document.querySelector` to both the up and down arrow. Using `addEventListener()`, update the value of the `h1` with a `class="money"`. The `h1` element should update every time the user clicks the up and down arrow. **REMEMBER** to update the value of `h1` you should be using `innerHTML`.
2. Get the information that the user puts into the form for the name, food preferance, and money. You should store this information in variables using `document.querySelector`. 
3. Attach and event listener to the button. When the user clicks the button, the values of name, food preference, and money should be updated. Log these to the console to make sure they are working. **NOTE**: Use the `.value` property to get the value from an input field. For example you could get their food choice by doing:
```javascript
var selection = document.querySelector('select');
button.addEventListener('click', function(event) {
  selection = selection.value
  console.log(selection)
}
```
4. Declare a recommendation function. The recommendation function should check (1) the amount of money the individual wants to spend and (2) their food preference. The function should update the screen that has `id=RestaurantText`. It is suggested that you start with just two options for each food preference. E.g. suggest one food Italian option if they want to spend more than $20 and one option if they want to spend less than $20.
5. Call the recommendation function every time the button is clicked. The text area should update every time the button is clicked.

## EXTENSIONS
- Alter the function so that it runs even if the person forgets to put in their name. It is likely it currently prints a message like "Hello undefined!" if they forget to put in their name. 
- The form doesn't seem to work if you change your options after selecting the button. Explore how to use `document.getElementById("IdOfElement").value` to fix this issue.
- Maybe the user **REALLY** doesn't want to make a decision and just wants the app to give them a random option regardless of food type or cuisine. Create a random choice button on `index.html` and randomly return a choice for them. It is suggested that you explore how to use `Math.random()` using the [documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random).
- In addition to a suggestion, return a picture of the restaurant, the restaurants website, and a location that they can go to in order to get their food
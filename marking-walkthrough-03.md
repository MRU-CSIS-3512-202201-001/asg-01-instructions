# Marking Walkthrough - Milestone 3 [WIP - not complete as of 2022-01-26]


These are the steps that I will take when I assess your submission. You can use this to figure out which requirements you've completed.

1. Head over to the student's GitHub repo created by GH Classroom [1] and confirm it has:
   1. a file called `default.html` [10], and
   2. a README.md with their name and a working hyperlink to `default.html` [2], and
   3. the Feedback pull request intact [3], and
   4. the `movie-data.json` file [8], and
   5. the `movieHelpers.js` file [9]

2. Stay in the repo and do some digging into the code:
   1. does `.eslintrc.json` contain the "no-var" property? [7]
   2. does `default.html` link to `movieHelpers.js`? [10]
   3. does `movieHelpers.js`:
      1. create an array of movie objects using JSON.parse? [20],
      2. have a constructor function called `MovieCollection` that 
         1. takes in ONE movie array arg, and 
         2. has an `all()` method returning an array of alphabetically-sorted movies, and
         3. has a `between()` method that takes in a lower and upper year bound, returning an array of alphabetically-sorted movies between those years inclusive, and
         4. uses reasonable array methods, and
         5. uses one or more arrow functions? [21]
      3. have a statement that creates a variable from the constructor? [22]


3. Click on the hyperlink in the README. It should go to a netlify url [2] and that url should have a site name in the proper format [4].

4. Copy the url for the app and check it through both the CSS validation service [5] and markup service [6].

5. Pop open the console. 
   1. Is an array of 666(!) alphabetically-sorted movies shown? [23]
   2. Is an array of 23 alphabetically-sorted movies shown? [24]

6. Looking at `default.html` in the browser, do I see
   1. a header with the content `COMP 3512 Assignment 1`? [11]
   2. an obvious way to filter movies by title? [12]
   3. an obvious way to filter movies before, after, and between years? [13]
   4. an obvious way to filter movies below, above, and between ratings? [14]
   5. an obvious way to clear all filters? [15]
   6. an obvious way to toggle the filter visibility? [16]
   7. 3 different movies from the JSON [17], displaying appropriate title, year, rating, and a way to view details [18]? 
   8. an obvious way to sort movies by title, year, and rating? [19]
   
7. Check how the page looks at Mobile L and Laptop L sizes. Is there anything jarring that jumps out about the layout at either size? [25],[26]

8. How does the site look at Laptop L size? How are colours, whitespace, alignment? [27]
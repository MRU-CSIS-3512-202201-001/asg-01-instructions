# FAQ

More recent questions will be near the top.

#### Q. How do you deploy default.html instead of index.html on Netlify?

> _A. You don't! Your Netlify site always has all the code from your GitHub repository. You need to change the `README.md` file in your repository so that it has a link to the URL of your `default.html` file._ 

#### Q. For RS5 [23] when you ask for the movies to be sorted alphabetically do you want them to have all their attributes or do you want me to map/filter it to only titles?

> _A. You're sorting an array of movie objects, so the result should be a sorted array of movie objects._ 

> _A. One of the Notes in RS4 says: "To populate the content for the 3 movies you choose, you'll have to dig through the movie-data.json file and do some copy and pasting."_ 

#### Q.  For the 3 movies that are shown in the List/Matches section can they be movies we choose or do they have to be from `movie-data.json`?

> _A. One of the Notes in RS4 says: "To populate the content for the 3 movies you choose, you'll have to dig through the movie-data.json file and do some copy and pasting."_ 

#### Q. For the rating, the slider is it necessary we have the numbers that go along with the sliders?

> _A. Technically, no - but the user of the site will need to know **somehow** what number they're providing. Remember that the diagrams are recommendations and it's certainly ok to do things differently than "what's in the picture" as long as the necessary functionality is there._ 

#### Q. When I try and put something like `const content = (json stuff in backticks)` VS Code says I have the problem: `Expected a JSON object, array or literal.`

> _A. VS Code is technically right! By tossing that JavaScript const/variable declaration in a file with a json extension, you've technically made the contents of that file invalid JSON! You can still use your const/variable in your `movieHelpers` code. FWIW, I'm not a big fan of this way of doing things - it's a hack, but it's a hack that works._ 

#### Q. My files aren't formatting when I save and I know I have Prettier installed.

>_A. Did you run `npm install` in the terminal after you cloned your repo? If not, the tools (in particular eslint and prettier) won't work correctly. You'll need to get into the habit of doing that for all tutorials and all assignments._ 

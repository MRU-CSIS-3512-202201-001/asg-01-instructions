# FAQ

More recent questions will be near the top.

#### Q. If I'm supposed to put all 3 Views in one file (index.html), isn't that going to be a mess? Not to mention the CSS...

> _A. It can definitely be quite ugly. But remember that a lot of the content should be created via JS! How far you take this is up to you: you could wind up having lots of empty div containers that you populate with JS functions. As for the CSS, it can be separated into reasonable files that target a given View, with some common CSS rules  pulled out into a global CSS file._


#### Q. How am I supposed to make sure my page serves up the properly-sized images? I don't want to be dinged like I was for milestone 3.

> _A. Just get the browser to do all the work by using an `<img>` tag that uses the `srcset` attribute. There is (as always) an [excellent article on MDN](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images#resolution_switching_different_sizes) about this._ 

#### Q. Do I need to use forms?

> _A. Nope. You will for assignment 2, when you need to talk to back-end code...but here? Not necessary. (You could use one if you wanted to change the submit behaviour via JS, but I'm not convinced it would be worth the effort!)_ 

#### Q. I'm confused about the whole "there should only be an index.hml now" thing.

> _A. In a single page application, you literally have a single page, almost always called `index.html`. The markup from your previous milestones - the markup for your index.html, default.html, and details.html - can now all go in one file: `index.html`. You'll likely want to place the markup in `<div>s` of some sort, so you can hide/show them easily when the need arises._ 

#### Q. How do I get the movie posters on the default page?

> _A. Take a boo at item 9 in the [assignment pdf](comp-3512-asg-1-winter-2020-current.pdf)._ 


#### Q. How do you deploy default.html instead of index.html on Netlify?

> _A. You don't! Your Netlify site always has all the code from your GitHub repository. You need to change the `README.md` file in your repository so that it has a link to the URL of your `default.html` file._ 

#### Q. For RS5 [23] when you ask for the movies to be sorted alphabetically do you want them to have all their attributes or do you want me to map/filter it to only titles?

> _A. You're sorting an array of movie objects, so the result should be a sorted array of movie objects._ 

#### Q.  For the 3 movies that are shown in the List/Matches section can they be movies we choose or do they have to be from `movie-data.json`?

> _A. One of the Notes in RS4 says: "To populate the content for the 3 movies you choose, you'll have to dig through the movie-data.json file and do some copy and pasting."_ 

#### Q. For the rating, the slider is it necessary we have the numbers that go along with the sliders?

> _A. The updating of the numbers will happen via JS, so you can ignore this for now. You'll have this functionality as a requirement on milestone 5. Good catch - and this totally slipped under my radar._ 

#### Q. When I try and put something like `const content = (json stuff in backticks)` VS Code says I have the problem: `Expected a JSON object, array or literal.`

> _A. VS Code is technically right! By tossing that JavaScript const/variable declaration in a file with a json extension, you've technically made the contents of that file invalid JSON! You can still use your const/variable in your `movieHelpers` code. FWIW, I'm not a big fan of this way of doing things - it's a hack, but it's a hack that works._ 

#### Q. My files aren't formatting when I save and I know I have Prettier installed.

>_A. Did you run `npm install` in the terminal after you cloned your repo? If not, the tools (in particular eslint and prettier) won't work correctly. You'll need to get into the habit of doing that for all tutorials and all assignments._ 

# Assignment 01 - Milestone 03

**Due February 02 (W) @ 9 PM**

**Worth 2% of your final grade**

**Content in this milestone document takes precedence over anything you read in the [assignment pdf](comp-3512-asg-1-winter-2020-current.pdf) and previous milestones.**

## Overview

This third milestone will involve getting your Movie Details View up. You will also be working with different sources of movie information, with the goal of extracting the information you need for the different page views (Default and Movie Details) from these sources.

This is the first of four milestones you will be working with your teammate(s) - it's important to start off strong and set a good tone with your partner(s). I'll provide some advice (if you want it) later in these docs.

## Viewing the Data

You'll need to dig through some fairly large JSON files (especially `credits.json` - that thing is a **beast**) to do some of the tasks in this milestone.

In their current state, it's super-hard to figure out what's going on in those files. I strongly recommend viewing them in an online JSON viewing tool to make sense of the seeming chaos. I've tried http://jsonviewer.stack.hu/ and https://jsonformatter.org/json-viewer for this and have been reasonably happy. **Don't try and open up `credits.json` in one of these viewers...there's a reasonable chance it'll cause your browser to burst into flame - use the `credits-brief.json` instead - it's there to give you an easy way to view the structure of the full-sized `credits.json`.**

## The Starting Repository

You will be working in a new repository, one that is set up for teams. Each member of the team has admin access to that repo - this will be both useful...and dangerous. Try not to nuke your (and your teammates') stuff.

The starting repo is here: https://classroom.github.com/a/Yd1563o5

When you accept this repo, you'll be asked to select a team:

![team selection](images/team-selection.png)

**Join the team you were told you are on. Please do NOT create a new team.**

## Your Mark

As with the first milestone, your mark will depend on which requirements sections (see below) you complete.

### The Ladder
|     Completed Req's Sections      | Grade Level | Corresponding % |
| :-------------------------------: | :---------- | :-------------: |
|               None                | Level 0     |       0%        |
| RS0 + Partial RS1,RS2<sup>1</sup> | Level 1     |       25%       |
|             RS0 - RS1             | Level 2     |       55%       |
|             RS0 - RS2             | Level 3     |       65%       |
|         RS0 - RS3 (Fair)          | Level 4     |       75%       |
|         RS0 - RS3 (Good)          | Level 5     |       88%       |
|       RS0 - RS3 (Excellent)       | Level 6     |       98%       |

_<sup>1</sup> If you get all of R0 done and at least part of RS1 **and** RS2 complete, you will get a Level 1 instead of a Level 0._

__


## The Requirements Sections

As I adjust to working with requirements marking, I will make changes based on experiences with previous milestones. This is called learning. :)

### RSO. Basic Requirements

_These requirements are all supposed to be very easy to complete - but also fundamental to your success (and to making the marking of your work easier for me). Skipping or being careless with these is a bad idea, because your mark becomes hella-low. None of us wants that._

- [ ] [1] The code for your site is located in the GitHub repo created by accepting the GitHub Classroom assignment.
  
- [ ] [2] The `README.md` file in the repo contains the names of all team members and a **working** hyperlink to the Netlify URL of the page (`details.html`) you wish me to mark. (Meaning I should be able to click on the link and go to THAT page!)

- [ ] [3] The Feedback pull request in the repo has not been closed or merged. 

- [ ] [4] The site is hosted on Netlify and is called `comp-3512-w2022-a1-<team>`. For example, `comp-3512-w2022-a1-team04`.

- [ ] [7] You do NOT have the `movie-data.json` file from milestone 2 in your repo.

- [ ] [8] You DO have a `movieHelpers.js` file in your repo.

#### Notes

- _<sup>4</sup> You can choose one team member's Netlify account to be the source of the site, or even create a shared Netlify account for that purpose. Whatever works - I just want a working site to look at!_
- _<sup>4</sup> Notice that the site name has changed!_
- _<sup>7</sup> This will break your code from milestone 2. That is expected.I warned you that this kind of thing was gonna happen!_
- _<sup>8</sup> This file will have completely different contents from last time - see the [JavaScript requirements](#rs2-javascript-requirements) - not the contents from milestone 2._

---

### RS1. Movie Details View Requirements

_See items 11-13 on pages 6 & 7 of the [assignment pdf](comp-3512-asg-1-winter-2020-current.pdf) to get a feel for where you're eventually heading._

_As with milestone 2, the focus here is not yet on the functionality of the site, but on laying the groundwork for that functionality._

_DON'T let the illustration in the pdf limit your creative process - your page does NOT have to look like the illustration. As long as the information that must be available IS available, you're meeting the requirements!_

- [ ] [10] The Movie Details View page is a resource named `details.html` that connects to the external JavaScript file `movieHelpers.js`.

- [ ] [11] There is a header with the text `COMP 3512 Assignment 1`.

- [ ] [ ] The movie displayed on this page is taken from one of the movies in the data provided to you.

- [ ] [ ] The movie title is clearly visible.

- [ ] [ ] The poster for the movie is clearly visible and is shown at w185 size at mobile L and w342 size at laptop L.

- [ ] [ ] The cast of the movie is clearly visible when this page first loads.

- [ ] [ ] Each cast member has their name and character name clearly visible.

- [ ] [ ] The cast of the movie is ordered by the `order` field, ascending.

- [ ] [ ] There is an obvious way to view the crew of the movie.

- [ ] [ ] Each crew member has their name, department, and  clearly visible.

- [ ] [ ] The crew of the movie is ordered alphabetically, first by department, then by name.

- [ ] [ ] There is an obvious way to close this Details view and return to the Default View.

- [ ] [ ] There is an obvious way to have the browser speak the movie title.

- [ ] [ ] **All** of the following are either clearly visible or clearly accessible from this page:

    - [ ] release date
    - [ ] revenue, formatted appropriately
    - [ ] runtime, formatted appropriately
    - [ ] tagline
    - [ ] IMDB link
    - [ ] TMDB link
    - [ ] overview
    - [ ] ratings (includes **all** of popularity, average, and count)
    - [ ] companies
    - [ ] countries
    - [ ] keywords
    - [ ] genres

- [ ] [ ] All CSS on `details.html` that is "yours" is declared valid by the [W3C CSS Validation Service](https://jigsaw.w3.org/css-validator/).

- [ ] [ ] All HTML on `details.html` is declared valid by the [W3C Markup Validation Service](https://validator.w3.org/).

#### Notes

- _This will force you to dig around in the JSON and get used to spelunking through data. This is a useful experience!_
- _The entire cast does not have to be visible all at once. This goes for the crew._

---

### RS2. JavaScript Requirements

There are a number of TODO items in `movieHelpers.js` Each TODO corresponds to a requirement, which I'll repeat here as well.

- [ ] An array of movie details, created from `movie-details.json` is present in `movieHelpers.js`.

- [ ] An array of credits, created from `credits.json` is present in `movieHelpers.js`.

- [ ] An array of keywords, created from `keywords.json` is present in `movieHelpers.js`.


#### Notes

---

### RS3. Visual Design Requirements


- [ ] [25] The `details.html` page has a reasonable layout with no glaring issues at Laptop L size.

- [ ] [26] The `details.html` page has a reasonable layout with no glaring issues at Mobile L size.

- [ ] [27] The visual design is portfolio-level quality. I'll be looking for generous use of whitespace, alignment of items, contrast of text in size and weight, good use of color (including accents), non-distorted images, etc.

#### Notes

- _I'll evaluate [xxx] as being one of Fair, Good, or Excellent. This will be purely a subjective thing, I'm afraid. If the level of [27] is not considered at least Fair, that requirement will be considered unmet._
- _Simply following the illustrations in the pdf will get you a Fair at best._

--- 

## Teamwork

### Communication

### Trello

### GitHub Habits

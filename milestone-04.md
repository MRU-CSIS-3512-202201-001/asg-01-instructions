# Assignment 01 - Milestone 04 (WIP - NOT OFFICIALLY RELEASED)

**Due February 09 (W) @ 9 PM**

**Worth 2% of your final grade**


**Content in this milestone document takes precedence over anything you read in the [revised assignment pdf](comp-3512-asg-1-winter-2020-v2.pdf) and previous milestones.**

## Overview

The fourth and fifth milestones are firmly focused on using JavaScript to get content on the page and to deal with all the different events that can happen when users interact with your pages.

Because of the large number of events you need to deal with, visual design is going to take a back seat in the marking of this and the following milestones. That being said, I will be taking a look at your pages periodically and providing you with feedback that I suggest you act on before the final milestone!

## Major Updates to PDF

There have been a lot of changes to the original version of the assignment. You should definitely read it, especially all the orange parts. There are a lot of orange parts.

There will be further changes to this doc over the next few weeks. Welcome to the Desert of Shifting Requirements! Just like when you're dealing with real clients! Yay?

## Things To Put On Your Radar

The following are things that will NOT be involved in your mark for this milestone or milestone 5...but will most definitely be involved in your mark for the final milestone.

I'm just telling you this so you can plan ahead and not be caught off-guard.

### Visual Design

Your final project is expected to have a unified, professional look. Take a look at the  visual design requirements section of [milestone 3](milestone-03.md) to get a feel for how this aspect of your work will be marked on the final milestone.

I will pop onto your sites periodically to nose around and provide comments on what I see. This should give you opportunities to make improvements before the final milestone.

### Code Quality

Functional code is ok - but if you're going to develop code for a living, you can't just focus on making stuff that gets the job done. You also has to create code that is expressive enough to be understood and modified by others (and, humourously, one of those others might be your future self).

Your code should follow [these guidelines](design-guidelines.md) to attain full marks for your final milestone.

I will dig into your repositories periodically to nose around and provide comments on what I see with your code. This should give you opportunities to make improvements before the final milestone.

### Script Organization

You shouldn't have one big-ass (pardon my French) file that holds all the JS for your site - that's just a nightmare for external parties (ahem, me) and yourself to navigate. Also, just having one file guarantees that you're going to enter merge conflict hell when it comes to working together with your teammates in Git.

You will need to have multiple files that hold site scripts to get full marks for the final milestone. You will have to consider how best to divide up your code. For example, you could divide things up by View (so 3 scripts there, 1 for each view). Or maybe divide things up by types of events (filter-related, search related, etc). Or some other way that works for you. Feel free to look for advice online and experiment - just don't put everything in one file. :)


## Your Mark

**Please read this section carefully, as it's quite different than what you've seen in the first 3 milestones!**

Your marks this time - and for milestone 5 - will be based mostly on how many [events](events.md) you can get done. (I say "mostly", because there are still a few requirements that you must do.)

### The Ladder of Marks
| What You've Done | Grade Level | Corresponding % |
| ---------------- | :---------: | :-------------: |
| RS0 incomplete   |   Level 0   |       0%        |
| ---              |     ---     |       ---       |
| RS0 only         |   Level 2   |       55%       |
| RS0 + 5 events   |   Level 3   |       65%       |
| RS0 + 10 events  |   Level 4   |       75%       |
| RS0 + 15 events  |   Level 5   |       88%       |
| RS0 + 20 events  |   Level 6   |       98%       |

---

LOCAL/SESSION storage - you need to look this stuff up on your own


## The Requirements Sections

As I adjust to working with requirements marking, I will make changes based on experiences with previous milestones. This is called learning. :)

### RSO. Restrictions

_These requirements are all supposed to be very easy to complete - but also fundamental to your success (and to making the marking of your work easier for me). Skipping or being careless with these is a bad idea, because your mark becomes hella-low. None of us want that._

- [ ] [1] The code for your site is located in the GitHub repo created by accepting the GitHub Classroom assignment.
  
- [ ] [2] The `README.md` file in the repo contains the names of all team members and a **working** hyperlink to the Netlify URL of the page (`details.html`) you wish me to mark.

- [ ] [3] The Feedback pull request in the repo has not been closed or merged. 

- [ ] [4] The site is hosted on Netlify. 
  
- [ ] [5] Your site is called `comp-3512-w2022-a1-<team>` in Netlify. For example, `comp-3512-w2022-a1-team04`.

- [ ] [6] You do NOT have the `movie-data.json` file from milestone 2 in your repo.

#### Notes

- _<sup>2</sup> Meaning I should be able to click on the link and go to THAT page!_
- _<sup>4</sup> You can choose one team member's Netlify account to be the source of the site, or even create a shared Netlify account for that purpose. Whatever works - I just want a working site to look at!_
- _<sup>5</sup> Notice that the site name has changed!_
- _<sup>6</sup> This will break your JS code from milestone 2 - but shouldn't be in this milestone anyway. I warned you that this kind of thing was gonna happen!_

---

### RS1. Movie Details View Requirements

_See items 11-13 of the [assignment pdf](comp-3512-asg-1-winter-2020-current.pdf) to get a feel for where you're eventually heading._

_As with milestone 2, the focus here is not yet on the functionality of the site, but on laying the groundwork for that functionality._

_DON'T let the illustration in the pdf limit your creative process - your page does NOT have to look like it. As long as the information that must be available IS available, you're meeting the requirements!_

- [ ] [7] The Movie Details View page is a resource named `details.html` that connects to the external JavaScript file `movieHelpers.js`.

- [ ] [8] There is a header with the text `COMP 3512 Assignment 1`.

- [ ] [9] The movie displayed on this page is taken from one of the movies in the data provided to you.

- [ ] [10] The movie title is clearly visible.

- [ ] [11] The poster for the movie is clearly visible and is shown at w185 size at mobile L and w342 size at laptop L.

- [ ] [12] The cast of the movie is clearly visible when this page first loads.

- [ ] [13] Each cast member has their name and character name clearly visible.

- [ ] [14] The cast of the movie is ordered by the `order` field, ascending.

- [ ] [15] There is an obvious way to view the crew of the movie.

- [ ] [16] When the crew is viewed, each crew member has their name, department, and job clearly visible.

- [ ] [17] The crew of the movie is ordered alphabetically, first by department, then by name.

- [ ] [18] There is an obvious way to close this Details view and return to the Default View.

- [ ] [19] There is an obvious way to have the browser speak the movie title.

- [ ] [20] **All** of the following are either clearly visible or clearly accessible from this page:

    - [ ] release date
    - [ ] revenue, _**formatted appropriately**_ <= emphasized for a reason, folks
    - [ ] runtime, _**formatted appropriately**_ <= ditto
    - [ ] tagline
    - [ ] IMDB link <= must be working
    - [ ] TMDB link <= must be working
    - [ ] overview
    - [ ] ratings (includes **all** of popularity, average, and count)
    - [ ] companies
    - [ ] countries
    - [ ] keywords
    - [ ] genres

- [ ] [21] All CSS used in `details.html` that is "yours" is declared valid by the [W3C CSS Validation Service](https://jigsaw.w3.org/css-validator/).

- [ ] [22] All HTML in `details.html` is declared valid by the [W3C Markup Validation Service](https://validator.w3.org/).

#### Notes

- _<sup>9</sup> You will need to dig through the different JSON files to piece together the data you need to display on the page. This will be tedious, but it WILL give you a much better idea how the different sources of information you will be using in the final product fit together and how they are structured._
- _<sup>11</sup> The lightbox effect for the poster is not needed for this milestone - it will be coming later._
- _<sup>12</sup> The entire cast does not have to be visible all at once. This goes for the crew, too._
- _<sup>18,19</sup> These don't have to be working yet._
- _<sup>20</sup> There's a blurb on making working IMDB and TMDB links in item 11 of the [pdf](comp-3512-asg-1-winter-2020-current.pdf)._
- _Consider where you might put some YouTube video links in your design, as I'm pretty sure that will be a requirement in a later milestone. (see item 14 in the  [pdf](comp-3512-asg-1-winter-2020-current.pdf))._

---

### RS2. JavaScript Requirements

There are a number of TODO items in `movieHelpers.js` Each TODO corresponds to a requirement, which I'll repeat here as well.

_Fair warning: the code you write here will also need to change going forward. Don't get too emotionally attached to it. If it helps, remember that when you're coding, you're not just producing code - you're also building experience, which is infinitely more valuable._

- [ ] [23] An array of movie details, created from `movie-details.json` is present.

- [ ] [24] An array of credits, created from `credits.json` is present.

- [ ] [25] An array of keywords, created from `keywords.json` is present.

- [ ] [26] A constructor function called `Movie` is present that has ALL the behaviour described in the associated TODO.


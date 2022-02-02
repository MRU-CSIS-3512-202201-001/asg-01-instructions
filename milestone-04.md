# Assignment 01 - Milestone 04 (WIP - NOT OFFICIALLY RELEASED)

**Due February 09 (W) @ 9 PM**

**Worth 2% of your final grade**


**Content in this milestone document takes precedence over anything you read in the [revised assignment pdf](comp-3512-asg-1-winter-2020-v2.pdf) and previous milestones.**

## Overview

The fourth and fifth milestones are firmly focused on using JavaScript to get content on the page and to deal with all the different events that can happen when users interact with your pages.

Because of the large number of events you need to deal with, visual design is going to take a back seat in the marking of this and the following milestones. That being said, I will be taking a look at your pages periodically and providing you with feedback that I suggest you act on before the final milestone!

## Major Updates to PDF

There have been a lot of changes to the original version of the assignment. You should [definitely read it](comp-3512-asg-1-winter-2020-v2.pdf), especially all the orange parts. 

There are a lot of orange parts.

There will be further changes to this doc over the next few weeks. Welcome to the Desert of Shifting Requirements! Just like when you're dealing with real clients! Yay?

## Things To Put On Your Radar

The following are things that will NOT be involved in your mark for this milestone or milestone 5...but will most definitely be involved in your mark for the final milestone.

I'm just telling you this so you can plan ahead and not be caught off-guard.

### Visual Design

Your final project is expected to have a unified, professional look. Take a look at the  visual design requirements section of [milestone 3](milestone-03.md) to get a feel for how this aspect of your work will be marked on the final milestone.

I will pop onto your sites periodically to nose around and provide comments on what I see. This should give you opportunities to make improvements before the final milestone.

**WARNING** 

_I noticed a few folks were using tables for layout; the final milestone will NOT allow this, so make sure you use the time effectively over these next few weeks to remove any trace of tables from your `index.html`._

### Code Quality

Functional code is ok - but if you're going to develop code for a living, you can't *just* focus on making stuff that gets the job done. You also have to create code that is expressive enough to be understood and modified by others. Humourously, one of those others might be your future self!

Your code should follow [these guidelines](design-guidelines.md) to attain full marks for your final milestone.

I will dig into your repositories periodically to nose around and provide comments on what I see with your code. This should give you opportunities to make improvements before the final milestone.

### Script Organization

You shouldn't have one big-ass (pardon my French) file that holds all the JS for your site - that's just a nightmare for external parties (ahem, me) and yourself to navigate. Also, just having one file guarantees that you're going to enter merge conflict hell when it comes to working together with your teammates in Git.

You will need to have multiple files that hold site scripts to get full marks for the final milestone. You will have to consider how best to divide up your code. For example, you could divide things up by View (so 3 scripts there, 1 for each view). Or maybe divide things up by types of events (filter-related, search related, etc). Or some other way that works for you. Feel free to look for advice online and experiment - just don't put everything in one file. :)

### TMDB Attribution

Milestone 6 will have us pulling in info from the TMDB API and I want to make sure we're following the [guidelines for attribution that TMDB has laid out](https://www.themoviedb.org/about/logos-attribution). This means that you should be prepared to add their logo and a brief attribution notice on your Default and Details Views somewhere by milestone 6.

## Your Mark

**Please read this section carefully, as it's quite different than what you've seen in the first 3 milestones!**

Your marks this time - and for milestone 5 - will be based mostly on how many [events](events.md) you can get done. (I say "mostly", because there are still a few "regular" requirements that you must do.)

### The Ladder of Marks
| What You've Done          | Grade Level | Corresponding % |
|---------------------------|:-----------:|:---------------:|
| RS0 incomplete            |   Level 0   |       0%        |
| ---                       |     ---     |       ---       |
| RS0 + fewer than 5 events |   Level 2   |       55%       |
| RS0 + 5 events            |   Level 3   |       65%       |
| RS0 + 10 events           |   Level 4   |       75%       |
| RS0 + 15 events           |   Level 5   |       88%       |
| RS0 + 20 events           |   Level 6   |       98%       |

---

LOCAL/SESSION storage - you need to look this stuff up on your own


## The Requirements Sections

As I adjust to working with requirements marking, I will make changes based on experiences with previous milestones. This is called learning. :)

### RSO. Basic Requirements

Read these carefully. Do them.

- [ ] [1] The Feedback pull request in the repo has not been closed or merged. 

- [ ] [2] There are no movie poster images in your repository.

- [ ] [3] All JavaScript used is present in external files. **This means NO embedded or inline JS is present.**

- [ ] [4] The **only** html present in your repository is `index.html`.

- [ ] [5] The `innerHTML` property is not used in any of your JS files.

- [ ] [6] All HTML in `index.html` is declared valid by the [W3C Markup Validation Service](https://validator.w3.org/).

- [ ] [7] There is a `displayDefault` function available from the console when `index.html` is visited. Details for the method are discussed [below](#the-displaydefault-function)



#### Notes

- _<sup>3</sup> If you don't know what this means, look at Figure 8.4 (p. 357) in the text, or look it up somewhere. 
- _<sup>6</sup> CSS validation is no longer a requirement._

---

### The `displayDefault` Function

You and I will both find it useful if there is a way to view the Default View, pre-populated with movies. To that end, you must create a function that allows you (and me) to do that from the console.

Here are the requirements for this function:

- [ ] It must be called `displayDefault`.
- [ ] It must have 1 parameter: `numMovies`.
- [ ] It must be callable from the console.
- [ ] It must have this behaviour:
  - [ ] It shows the Default View and hides the other 2 Views.
  - [ ] If it is called with `numMovies` equal to 0, the Default View shows no movies.
  - [ ] If it is called with `numMovies` as an integer > 0, the Default View shows `numMovies` randomly-chosen movies. (Look up on how to generate random numbers in JS.)
  - [ ] If it is called with no argument, the Default View shows exactly these movies:
  
    ```
    1. Aliens
    2. Alien
    3. The Thing
    4. Dark City
    5. Around the World in 80 Days
    6. The Prestige
    7. The Mask of Zorro
    8. Superman II
    9. Fast Times at Ridgemont High
    10. Ted
    ```

  - [ ] If it is called with any other arguments, I don't care what happens.

## Submission Requirements

Since y'all have a ton of flexibility in choosing which events to work on, I need some way for us to easily track what events you've completed so that I can focus on marking those specific things.

To do this, I am requiring groups to use the projects feature of your team's GitHub repo introduced in the [teamwork doc](teamwork.md) when I release milestone 3.

You will see that you have an `events` project in your team's GitHub repo shortly before or after the time I release this current milestone. In it, I've placed all the events that a fully-functioning application requires. _There's a reasonable chance that some additional events may be added, though I think I've got most of the ones we need._

When your team has completed an event, you should move it to the `Done` column in your project. I will use the events I see in that column when I mark.

### Extensions

For this milestone (and likely milestone 5), I will not be accepting any extension requests - when I get around to assessing your team's work, I will assess what's available to me at that time. _I will start marking early in the morning of Thursday, February 10. I'll pick teams at random ( literally - I'll use an online random-number generator) and mark until all teams are marked._
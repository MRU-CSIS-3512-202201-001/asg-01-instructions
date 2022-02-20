# Big List o' Events

## NEW: Searching vs Filtering

It's important that you understand the difference between _searching_ and _filtering_ in the context of this assignment.

### searching

**Searching** for titles is what a user does via the Home View:

1. they type in some text in the title search box, which will start autocompleting once the third letter is reached
2. they either accept an autocompletion suggestion (which enters that suggested movie title in the search box), or they ignore it and just go with whatever they typed
3. they hit the search by title button (allowing them to use Enter would sure be kind....) 
4. they are then taken to the Default View, where they see all movies that matched - even partially - the search box entry

### filtering

**Filtering** is what happens when you're in the Default View. You already have in front of you results of some kind: either a list of movies that matched a title search OR a list of your favourite movies. Now you want to _narrow down_ those results by applying restrictions (i.e. filters).

Filters do not start the search process over again! They only act on the results that have come from the Main View.


## About APIs & Local/Session Storage

Some of the following events refer to something called an **API**. We won't be covering that until week 5, so I'd suggest skipping those events until later...things get a bit weird and just eating copy pasta ain't gonna help you out here.

Some the events refer to **local storage** and **session storage**. This is covered in 10.4.1 of the text. You can find similar information if you look at [MDN's Web Storage API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API) page. These things are actually super-easy to use (and frankly, damn cool), so I think you can tackle events that use them without much difficulty.

## NEW: Events WITH COMMENTS

_Now that I've gone through an initial marking experience with people implementing these events, I think I can start to offer some useful comments as well. This makes things clearer, but longer. Sorry. Classic tradeoff!_


### Home View Events

- [ ] [HOME.1] When a user arrives on this page, the title search box should be empty.
  
    _You can get to the Home View from the Default and Details Views, right? So don't forget to handle arriving here from there._

- [ ] [HOME.2] [API] When a user types in the movie title search box, from the 3rd letter onward,  titles of movies starting with the entered letters (case-insensitive) appear as per any standard autocomplete search box.
  
- [ ] [HOME.3] [API] When a user chooses a movie from an autocomplete result list, the clicked-on movie appears in the title search box.
  
- [ ] [HOME.4] A user should not be allowed to search for a title when the title search box is empty.

    _There are ways to do this without the obnoxiousness of an alert. Notice that this doesn't say you need to WARN or CHASTISE the user. Just **prevent** them..._
  
- [ ] [HOME.5] When a user chooses to show matching movies, but there is no movie that matches or partially matches the title, the Home View is hidden and the Default View is shown, with a clear indication that no matching movies were found. 

    _When a user gets to your Default View, if there are no movies there, they might think "oh - this site is broken and doesn't work properly"...unless there's some kind of message there that lets them know that their search/favourite viewing produced no results!_
  
- [ ] [HOME.6] When a user chooses to show matching movies, and one or movies match, or partially match, the title search entry, the Home View is hidden and the Default View is shown, displaying all movies that match in alphabetic title order. 

    _This is a "matches anywhere in the title" match. Not a "start of the title" match._
  
- [ ] [HOME.7.EDITED] When a user chooses to show favourited movies, the Home View is hidden and the Default View is shown with all movies that are stored in local storage. This might be no movies, in which case this is clearly indicated. If there are movies, they are in alphabetic order by title.

    _The same concept from HOME.5 applies here - let your user know that if there are no movies, that's because they have no favourites, not because your website is functionally challenged._

- [ ] [HOME.8.NEW] A user should not be allowed to show their favourited movies when the title search box has text in it.

    _Same warning as with HOME.4._

- [ ] [HOME.9.NEW] After initiating a title search, a loading animation is visible until the movie list is ready to be populated. 

### Notes

- _<sup>1</sup> You don't have to worry about the user coming back to this page through use of the browser's Back button._
- _<sup>2</sup> If you have the labs, lab exercise 10-6 covers this. If not, you have some digging to do!_
- _<sup>5,6</sup> Behind the scenes, movie objects matching the title search term must be stored in the browser's session storage._


### Default View Events

- [ ] [DEFAULT.1.EDITED] When a user arrives on this page from the Home View, the title and all year filters are empty and all ratings filters have a value of 0. We'll cause these the **starting values**.

    _The confusion the previous version of this caused rests firmly on me. I think the edited version is much clearer. And easier to implement._

- [ ] [DEFAULT.2] When a user arrives on this page from the Details View, all filters have the contents they had when the user left the Default View.

- [ ] [DEFAULT.3.EDITED] A user should not be allowed to apply filters when all filters have their starting values.

    _Same comments as for HOME.4._

- [ ] ~~[DEFAULT.4] When a user attempts to clear filters, but no filters have been entered, nothing should change on the page.~~

    _Removed, because in the end, this is just confusing._
   
- [ ] [DEFAULT.5] When a user chooses to enter data for a filter (using whatever means are available on the page), the numeric value of the entered data is clearly visible.

    _The year and ratings filters don't **have** to be text inputs and sliders, right? This event was me trying to say "whatever way you decide to handle the numeric year and rating filters, make sure the user clearly sees what numbers they're entering"._

- [ ] [DEFAULT.6.EDITED] When a user chooses to enter data for a filter (using whatever means are available on the page), if any other filter has data in it, that filter returns to its starting value.

    _Changed "default" to "starting"._

- [ ] [DEFAULT.7] When a user chooses to apply a title filter, if this returns no results, that is clearly indicated to the user on this page.

    _This, and the other similar ones here is just saying the same thing as HOME.5: make sure you don't just show no results, because the user doesn't know whether no results == developer being lax, or no results == the filter filtered everything out!_

- [ ] [DEFAULT.8] When a user chooses to apply a title filter, if this returns results, those results are displayed in alphabetic order by title on this page.

- [ ] [DEFAULT.9] When a user chooses to apply a "before year" filter, if this returns no results, that is clearly indicated to the user on this page.

- [ ] [DEFAULT.10] When a user chooses to apply a "before year" filter, if this returns results, those results are displayed in alphabetic order by title on this page.

- [ ] [DEFAULT.11] When a user chooses to apply "after year" filter, if this returns no results, that is clearly indicated to the user on this page.

- [ ] [DEFAULT.12] When a user chooses to apply "after year" filter, if this returns results, those results are displayed in alphabetic order by title on this page.

- [ ] [DEFAULT.13] When a user chooses to apply a "between year" filter, if this returns no results, that is clearly indicated to the user on this page.

- [ ] [DEFAULT.14] When a user chooses to apply a "between year" filter, if this returns results, those results are displayed in alphabetic order by title on this page.

- [ ] [DEFAULT.15] When a user chooses to apply a "below rating" filter, if this returns no results, that is clearly indicated to the user on this page.

- [ ] [DEFAULT.16] When a user chooses to apply a "below rating" filter, if this returns results, those results are displayed in alphabetic order by title on this page.

- [ ] [DEFAULT.17] When a user chooses to apply a "above rating" filter, if this returns no results, that is clearly indicated to the user on this page.

- [ ] [DEFAULT.18] When a user chooses to apply a "above rating" filter, if this returns results, those results are displayed in alphabetic order by title on this page.

- [ ] [DEFAULT.19] When a user chooses to apply a "between rating" filter, if this returns no results, that is clearly indicated to the user on this page.

- [ ] [DEFAULT.20] When a user chooses to apply a "between rating" filter, if this returns results, those results are displayed in alphabetic order by title on this page.

- [ ] [DEFAULT.21.EDITED] When a user chooses to clear filters and filters have been entered, all filters return to their starting values.

    _Changed "default" to "starting"._
   
- [ ] [DEFAULT.22] When a user chooses to toggle the visibility of the filters when they are visible, the filters are removed from view with some sort of transition effect (animation or fade); when this transition is complete, there must be an obvious way to bring the filters back into view again.

    _Be thoughtful with this - those filters take up real estate on the page, right? Removing the filters should free up some real estate, not just leave a gap on the page!_ 
    
- [ ] [DEFAULT.23] When a user chooses to toggle the visibility of the filters when they are not visible,the filters are returned to view with some sort of transition effect (animation or fade); when this transition is complete, there must be an obvious way to remove the filters from view again.

- [ ] [DEFAULT.24] When a user chooses to sort the visible movies in ascending order by title, all movies present (whether currently in view or not) are sorted in alphabetic order.

    _If this isn't working for you...you ARE using event delegation, right? Because it's a requirement in the pdf....Also, you DO provide a visual clue whether the current sort is ascending or descending, right?_

- [ ] [DEFAULT.25] When a user chooses to sort the visible movies in descending order by title, all movies present (whether currently in view or not) are sorted in reverse alphabetic order.

- [ ] [DEFAULT.26] When a user chooses to sort the visible movies in ascending order by year, all movies present (whether currently in view or not) are sorted in ascending year order.

- [ ] [DEFAULT.27] When a user chooses to sort the visible movies in descending order by year, all movies present (whether currently in view or not) are sorted in descending year order.

- [ ] [DEFAULT.28] When a user chooses to sort the visible movies in ascending order by rating, all movies present (whether currently in view or not) are sorted in ascending rating order.

- [ ] [DEFAULT.29] When a user chooses to sort the visible movies in descending order by rating, all movies present (whether currently in view or not) are sorted in descending rating order.

- [ ] [DEFAULT.30.EDITED] When a user chooses to view the details on a movie by clicking on its poster or title, the Default View is hidden and the chosen movie is shown in the Details View. **This is accomplished through event delegation.**
    
- [ ] [DEFAULT.31] When a user clicks on the header, the Default View is hidden and the Home View becomes visible.

- [ ] [DEFAULT.32] When a user favourites a movie, there is a clear indication that this has happened.

    _Icons for the win, folks. Buttons are...um...just...no. Unless it's a very well-styled button perhaps._

- [ ] [DEFAULT.33] When a user unfavourites a movie, there is a clear indication that this has happened.

- [ ] [DEFAULT.34.NEW] When a user clears the filters, the movies present when the user originally arrived on this View are all showing.

    _In other words, when your remove filters, you get the movies you started with!_

### Notes

- _<sup>15-20</sup> We will consider "rating" to be equal to the vote_average value in the movie details._
- _<sup>32,33</sup> Behind this scenes, favourited/unfavourited movies must be added/removed from the browser's local storage._

### Details View Events

- [ ] [DETAILS.1] When a user arrives on this page from the Default View, the details of the movie selected in the Default View are shown, as outlined in milestone 3.

- [ ] [DETAILS.2] When a user chooses to hear the title of the movie spoken, the movie title is spoken by the browser's Web Speech API.
  
- [ ] [DETAILS.3] When a user chooses to close the Details View, the Details View is hidden and the Default View becomes visible.
  
- [ ] [DETAILS.4] When a user clicks on the header, the Details View is hidden and the Home View becomes visible.

- [ ] [DETAILS.5] When a user clicks on the IMDB link, the page of the movie opens in IMDB in a new browser tab or window.

- [ ] [DETAILS.6] When a user clicks on the TMDB link, the page of the movie opens in TMDB in a new browser tab or window.

- [ ] [DETAILS.7] When a user clicks on the poster, a larger (w500 @ mobile L, w780 @ laptop L) version of the poster is displayed in a pop-up modal. (_Edit [2022-02-08]: you can skip the mobile modal, or make it smaller than w500._)

- [ ] [DETAILS.8] When a user wishes to view Cast information for the movie, this is possible.

- [ ] [DETAILS.9] When a user wishes to view Crew information for the movie, this is possible.


### Notes

- _<sup>7</sup> This modal must be generated with your own code, not via another library or framework._
- _<sup>8,9</sup> This is vague, but it can't be helped, as how folks are going to handle the display of cast/crew will vary wildly._


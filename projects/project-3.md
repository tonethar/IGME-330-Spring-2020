# Project 3 - Web App Mashup of Awesomeness!

## I. Overview

For this project you (and optionally a partner) are creating a JavaScript driven Web application that utilizes multiple Web services.

- Your goal is to create an application that does something useful easy to use, functional, and aesthetically pleasing.
- The app should serve a purpose - i.e it should be useful to *someone*
- *As a counter-example, **Otaku-za** - a (hypothetical) app that mashes up a Manga search API with a Pizza shop locator, is not actually useful*
- Ideally the experience will run in all modern browsers, but at a bare minimum it must run in recent versions of Chrome.
- The objective of this project is for you to demonstrate your mastery of HTML5/CSS/JS "rich media" programming in a web browser context
- You will be evaluated on:
    - the quality of the experience you create
    - the soundness of your programming
    - meeting the requirements detailed below
    - how far you went beyond what we did in class, as described below

<hr>

## II. Project Requirements

<a id="functionality"></a>

### II-A. Functional Requirements
1. You must use **TWO** distinctive web service APIs in your completed project:
    - i. Try to use an API that supports *CORS* (Cross-origin resource sharing) - but if it does not, you might be able to write a PHP proxy server to fetch the data
    - ii. **CAUTION:** if an API requires an API Key, be sure that there is a generous "free tier", and that the API does not have a short trial period. Approach the following APIs with caution:
      - The YouTube API is severely rate limited - AVOID
      - The Spotify API requires server authentication, and most of the sample code uses Node.js - AVOID 
      - Yelp uses server-side authentication - BUT we posted some sample code in myCourses that you could adapt for your use
      - "Sports Scores" APIs tend to have very short trial periods (7-10 days) and onerous rate limits - AVOID!
        - but some students have had luck with this one --> https://developer.sportradar.com
      - Always verify that the API returns current data. There's a "gasoline prices" API out there that has 4 year-old data ...
    - iii. Here are some lists of web services:
      - https://github.com/toddmotto/public-apis
      - https://github.com/abhishekbanthia/Public-APIs
      - [www.programmableWeb.com/apis](http://www.programmableWeb.com/apis) has links to thousands of APIs - most free to use with sign-up
      - [developers.google.com](https://developers.google.com/) has over 50 APIs - sign up and then check out their API console
      - [Amazon Web Services (AWS)](https://aws.amazon.com)
      - [RapidAPI](https://rapidapi.com)
      - [Microsoft Azure](https://azure.microsoft.com/en-us/free/)
    - iv. APIs that utilize text:
      - [RiTa.js](https://rednoise.org/rita/)
      - [Wordnik API](https://developer.wordnik.com/faq)
    - v. Game APIs
      - [Giant Bomb Game API](http://www.giantbomb.com/api/)
      - [League of Legends API](https://developer.riotgames.com)
      - [Programmable Web - Game APIs](http://www.programmableweb.com/category/games/apis?category=20098)
    - vi. US Government Data:
      - [USGS Earthquake data](https://earthquake.usgs.gov/fdsnws/event/1/)
      - here's a video that runs through mapping earthquake data --> [Coding Challenge #57: Mapping Earthquake Data](https://www.youtube.com/watch?v=ZiYdOwOrGyc)
      - https://api.nasa.gov
      - [FBI Crime Data API](https://crime-data-explorer.fr.cloud.gov/api)
    - vii. Book information APIs:
      - [www.programmableweb.com/news/53-books-apis-google-books-goodreads-and-sharedbook](http://www.programmableweb.com/news/53-books-apis-google-books-goodreads-and-sharedbook/2012/03/13)
    - viii. Coronavarius:
      - https://rapidapi.com/collection/coronavirus-covid-19
      - https://data.humdata.org/dataset/novel-coronavirus-2019-ncov-cases
      - NYS Case Data: 
        - https://coronavirus.health.ny.gov/county-county-breakdown-positive-cases
        - https://health.data.ny.gov/Health/New-York-State-Statewide-COVID-19-Testing/xdss-u53e/data
        - https://health.data.ny.gov/api/views/xdss-u53e/rows.csv?accessType=DOWNLOAD
      - US County Boundaries: https://www.census.gov/geographies/mapping-files/time-series/geo/carto-boundary-file.html
      - Population data: 
        - https://www.census.gov/programs-surveys/acs/guidance/estimates.html
        - https://www.cdc.gov/csels/dsepd/ss1978/lesson3/section2.html
      - Hospitals: https://hifld-geoplatform.opendata.arcgis.com/datasets/hospitals/data
      - Grocery Stores: https://data.ny.gov/Economic-Development/Retail-Food-Stores/9a8c-vfzj/data
      - Zip Codes Tab areas: 
        - https://www.census.gov/programs-surveys/geography/guidance/geo-areas/zctas.html
        - https://catalog.data.gov/dataset/tiger-line-shapefile-2019-2010-nation-u-s-2010-census-5-digit-zip-code-tabulation-area-zcta5-na
    - ix. Others:
      - Woot deals --> [http://woot.wikia.com/wiki/API](http://woot.wikia.com/wiki/API)
      - Movie info --> [themoviedb.org/documentation/api](https://www.themoviedb.org/documentation/api)
      - Nearby restaurants --> [Yelp API](http://www.yelp.com/developers/documentation)
      - Current weather and forecasts --> [openweathermap.org/api](https://openweathermap.org/api)
      - Business and start-up info --> [data.crunchbase.com/v3.1/docs](https://data.crunchbase.com/v3.1/docs)
    - x. **Another Option - make your own API in PHP:**
      - the data should be useful and not an otherwise widely available subset from another public API
      - you should have **a lot** of data - 50 to 100 records at least
      - the API must have at least 2 [*endpoints*](https://dev.socrata.com/docs/endpoints.html), and be "queryable" - meaning that parameters can be passed to it, and it won't just return the same JSON file everytime it is called
      - the example in the *Project 3 Proposal* dropbox was a database of ice cream stands (which often don't show up in Yelp), similar things would be flea markets, farm stands, etc
      - or another custom dataset (a comprehensive RPG web service?), or ???
    - xi. Here are the "Blacklisted" APIs that you **MAY NOT** use for this project (but if you can envision a compelling use case, just ask us, in advance):
      - Any API from GIPHY - https://developers.giphy.com/docs/ (we love Giphy, but we don't want a bunch of "Giphy Finder++ Apps)
      - The iTunes Search API - https://affiliate.itunes.apple.com/resources/documentation/itunes-store-web-service-search-api/
      - Google Maps (use MapBox instead)
    - xii. **Important note:** - This is a Web programming class so I expect you to "roll your own" when it comes to adding Web service capability to your pages:
      - That means that JavaScript "widgets" that display (for example) Twitter feeds or the current weather are expressly forbidden
      - You have the knowledge to write these yourself if you desire this sort of functionality in your project.


2. You will automatically save the last term searched by the user and other UI *state* in the browser's local storage - this was covered in IGME-230/235 here --> [Web Apps 9 - WebStorage API](https://github.com/tonethar/IGME-230-Master/blob/master/notes/web-apps-9.md):
    - this will also be true of the other controls on the page (&lt;select> tags, radio buttons, checkboxes etc)
    - we are going to test this capability by typing in a search term, selecting some checkboxes, doing a search, and then closing the browser window. When we re-open the window, the user's last search term must be visible, and the rest of the UI should be in the same *state*


3) You must have a "reset" button that clears the search text field (in any) and resets other UI elements to their default state. This button will also clear out the values in local storage - the `.clear()` method accomplishes this  (Important: this "reset" button doesn't count towards the 3 control requirement below)


4. Other required controls - there will be a MINIMUM of 3 controls that a user can use to filter and display the results. Search buttons or similar don't count towards the 3 controls. For example, [GIF Finder](https://github.com/tonethar/IGME-230-Master/blob/master/notes/HW-gif-finder.md) has these controls:
    - a search button (which doesn't count, and the "reset" button mentioned above does not count either)
    - a search term field (&lt;input>) that the user types into
    - a pulldown (&lt;select>) that the user can use to limit the number of results

    -  **So you will need at least one additional kind of control. What kind of control to use depends on what parameters the web services will allow you to search them on. Here are some ideas:**
       - a **rating** pulldown - if we had this on the GIPHY HW then a user would be able to choose between viewing "G" and "PG" videos for example
       - a **sort by** pulldown to allow the user to view the results sorted A->Z, Z->A, by date, etc 
       - a **date** chooser to filter the results by date - https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/date
       - **next** and **previous** buttons - another really nice option is to allow the user to "page" through large numbers of results. In the GIPHY HW did you notice that we always get the same 100 "cat" GIFs back when we search?
         - This is because there are ***thousands*** of cat GIFs on GIPHY, and if we don't otherwise specify we will always get them returned from the web service starting at index 0, which means we always get the first 100 (index 0-99) back.
         - We can instead write code that requests a higher starting index.
         - In the GIPHY API this can be done by tracking and adding an `offset` value to the query string that is sent over to the API.


4. Optional features:
    - Firebase or a similar API to store data "in the cloud"
    - There's no rule against exceeding the minimum, and having 4 controls, or even 5!, if the app would benefit from them
  
<hr>

<a id="design"></a>

### II-B. Design & Interaction
1) Pleasing graphic design:
    - must be *usable*
    - minimally, it must be "not ugly"
    - the interface must not resemble the GIPHY homework's UI at all
    - an *embedded* font must be used - for example from https://fonts.google.com:
      - be cautious about using an embedded font - especially a cursive font - for UI labels
      - instead, utilize the embedded font on ornamental elements, like a title or copyright notice
    
2) Widgets are well labeled and follow interface conventions, for example:
    - radio buttons are for mutually exclusive options, checkboxes are for when you want to let the user choose *multiple* options --> https://delib.zendesk.com/hc/en-us/articles/203430309-Radio-button-vs-checkbox-what-s-the-difference-
    
3) Users should be able to figure out how to use the app with minimal instruction:
    - be sure to provide instruction and tooltips if necessary
    
4) User errors must be handled gracefully:
    - for example, if the user forgets to type in a search term before clicking the Search button, the app should tell the user something like "Please enter a search term first"
    
5) Users must know what *state* the app is in at all times:
    - for example, when they click the search button, there should some indication that a search is happening:
      - text that says "Searching for 'Tacos' near you" and so on
      - a "spinner" or other "indeterminate progress" animation --> [Google search "indeterminate progress"](https://www.google.com/search?q=indeterminate+progress&client=safari&rls=en&source=lnms&tbm=isch&sa=X&ved=0ahUKEwj-sNCal4neAhVr34MKHWKqA98Q_AUIDigB&biw=1036&bih=583)
      - here are some "spinner" images you could use (show them when the search starts, and hide them when the search ends): http://ajaxloaders.net/2012/10/spinner-loading-animations-set-1/
      
6) While the app doesn't need to be fully responsive, it should look good on a range of displays. 
    - For example, don't design it just to work on your huge 24" screen at home, as I'll be grading it on a laptop with a 15" screen
    - The main controls of the application must fit in a 1200x800 window (or smaller)

7) Optional Features:
    - Sound:
      - Subtle UI sound can be a nice extra
      - Keep your sound file sizes as small as possible. Primarily use MP3's; WAV's are OK for short sound effects
    - UI Animations:
      - https://www.creativebloq.com/features/create-cool-ui-animations-with-css
      - https://www.mockplus.com/blog/post/css-animation-examples
    - Canvas Drawing/Animation:
      - &lt;canvas> visualization of web service data can be a nice extra
      - Drawing libraries such as Pixi.js, Three.js, Processing.js and D3.js are allowed
      - Charting web services like Google Charts could also be a nice thing to use (and would count as a second web service)

<hr>

<a id="media"></a>

### II-C. HTML/CSS & Media
1) Valid HTML5 - https://validator.w3.org
    - Use HTML5 semantic and structural elements where practical
    
2) Valid CSS - https://jigsaw.w3.org/css-validator/
    - Most CSS is in an external style sheet
    
3) Utilize at least 3 HTML semantic elements such as &lt;nav>, &lt;main>, &lt;footer>, etc 

4) Images are properly optimized (both dimensions and file size) for Web delivery

5) An embedded font must be used

6) You ARE allowed and encouraged to use CSS frameworks on the UI for this project, such as:
    - https://bootstrap-vue.js.org
    - http://getbootstrap.com
    - http://materializecss.com
    - https://purecss.io
    - https://github.com/troxler/awesome-css-frameworks
    - if you build off of a CSS template you found on the web or LinkedIn Learning etc, that's fine, just give credit both in the code comments and in your final documentation

<hr>

<a id="code"></a>

### II-D. Code Requirements
1) ES6 Module Pattern required
    
2) Ajax - app utilizes the [`XHR`](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest) or [`Fetch`](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API) API

3) Use at least 1 ES6 custom class, written by you:
    - for example, if your web service was downloading and displaying state parks in a list, you could create a class called `StatePark` to model the data
    
4) Conventions and structure:
    - All code is in external JavaScript files
    - `let` and `const` must be used to declare variables - no `var` allowed!
    - D.R.Y. - Don't Repeat Yourself. Repeated blocks of nearly identical code must be factored out and placed in a separate function
    - Variable and function names must begin with a lowercase letter
    - Class names must begin with an uppercase letter
    - Well-commented code. Each and every function gets a comment indicating what it does
    
5) Be sure that the app functions as expected when posted to `banjo.rit.edu` - for example, be sure that there are not any security issues caused by using `http` instead of `https` in links to libraries and so on

6) It is expected and required that the code in the assignment (other than from approved libraries) is written by you. If you do end up using a small amount of code you found on the web, you must document where you got it from.  Give credit and a link for all code (fragments or otherwise) that are not written you. Failing to give credit opens you to charges of **academic dishonesty**:
   - examples of acceptable use for this project:
     - copying a GUID generating function "whole cloth" from StackOverflow - https://stackoverflow.com/questions/105034/create-guid-uuid-in-javascript
     - copying and lightly modifying code for a "hamburger" menu - https://www.google.com/search?q=vanilla+javascript+hamburger+menu
   - Cite the code source **both** in the source code itself as a comment, and in your final documentation
   - Be sure to make borrowed code "your own" as much as possible for example by simplifying or improving the clarity of the code,  using `let` or `const` instead of `var`, getting rid of inline event handlers (which are prohibited in this project) and so on
   - You do not need to cite code that you received from this semester's in-class exercises, demos or HW
   - **If you have any doubt about what is acceptable to "borrow", ask the professor *in advance* of using it**
   
6) **NOT allowed**:
    - jQuery DOM manipulation - for example `$.html()` - is NOT allowed
    - `var`
    - inline event handlers in your HTML ex. `<button onclick="alert('Hi!')">Click Me</button>`
    - `console.log()` calls (delete or comment them out)

<hr>

<a id="impact"></a>

### II-E. Impact
  - Does the app work as intended and do something useful?
  - Does the app functionality and programming go beyond what we did in class?
  - Is this project "portfolio quality" that you would not hesitate to show a potential employer?

<hr>

<a id="extras"></a>

### II-F. Extras
  - Add "some above and beyond" if you have time - be sure to call your efforts out in the documentation. Here are some ideas:
    - use of an MVVM framework like [Vue.js](https://vuejs.org) (which we covered in class) or [React](https://reactjs.org) is strongly encouraged
    - integrate some custom visualizations into your app using canvas or similar
    - use the [D3](https://d3js.org) visualization library
    - utilize a cloud storage service such as Firebase in some way. There were several extra credit Firebase exercises this semester that could get you started

<hr>

## III. Milestones (one submission per team please - make sure both team members' names are stated)
  - **Project Proposal** - see myCourses for details & due date/time
  - **Checkpoint #1** - see myCourses for details & due date/time
  - **Checkpoint #2** - see myCourses for details & due date/time
  - **Final project deliverable & documentation** - see myCourses for details & due date/time
  - **Demo reel** - 1 to 2 minute video demo of the final version of app (alternatively, have a Zoom meeting with us finals week to demo it)

<hr>

## IV. Documentation
  - As with Project 2, include a file where you document your process, cite any sources, tell me where to find anything special you want me to see, and also explain how you met the requirements. Finally, give yourself a numeric grade for the project that you feel fairly represents what its worth
  - If you worked in a team, explain what each team member did. Remember, everyone is responsible for contributing throughout the project, not just to one aspect

<hr>

## V. Grading


Your project will be graded on the following criteria:

| Criteria | Weight | Your Score |
| -------- | ------ | ---------- |
| **A. [Functionality](#functionality)** | **40** | |
|    1. TWO web services are used | |
|    2. Saves/restores last search term and other UI *state*  | |
|    3. Has "reset" button | |
|    4. Has other required Controls | |
|    - *Missing web services* | *(-20 each)* |
|    - *Does not save/restore UI state* | *(-10)* |
|    - *Missing reset button* | *(-10)* |
|    - *Missing other controls* | *(-10 each)* |
| **B. [Design & Interaction](#design)** | **20** | |
|    1. Visual design is at a minimum, usable and "not ugly" | |
|    2. Widgets are well labeled and follow interface conventions | |
|    3. Users should be able to figure out how to use the app with minimal instruction | |
|    4. User errors must be handled gracefully | |
|    5. The *state* the application is in is obvious | |
|    6. The app should look good on a range of displays. | |
|    - *Missing embedded font* | *(-5)* |
|    - *Missing "state" cues like status text or "spinners"* | *(-5)* |
|    - *Interface looks like GIF Finder HW* | *(-15)* |
|    - *Interface "broken" at 1200x800 or higher resolutions* | *(-10)* |
| **C. [HTML/CSS/Media](#media)**  | **10** | |
|    1. Valid HTML | |
|    2. Valid CSS | |
|    3. Uses HTML5 Semantic elements | |
|    4. Images properly optimized | |
|    5. Has embedded font (see above) | |
|    - *Fails HTML Validation* | *(-5)* |
|    - *Fails CSS Validation* | *(-5)* |
|    - *Most CSS is NOT in an external stylesheet* | *(-5)* |
|    - *Missing required HTML5 semantic elements* | *(-5)* |
|    - *Images larger than 50KB* | *(-2 each)* |
| **D. [Code](#code)**  | | |
|    - *ES6 Module pattern not used* | *(-25)* |
|    - *Ajax not used* | *(-25)* |
|    - *ES6 Custom Class missing* | *(-5)* |
|    - *Conventions NOT followed* | *(-1 to -5 per incident)* |
|    - *Code that is NOT allowed* | *(-1 to ? per incident)* |
|    - *Code shows errors in console* | *(-5 per incident)* |
|    - *App does not function on banjo* | *(-10)* |
|    - *App does not run locally or on banjo* | *(-10 to ?)* |
| **E. [Impact](#impact)**  | **30** | |
|    - If the app meets the requirements above, we will award a 20% in this category, which means the base overall grade is 90% | |
|    - *App functionality and programming goes beyond what we did in class* | *(+1 to +10)* |
|    - *App UI design goes beyond what we did in class* | *(+1 to +10)* |
|    - *App is "portfolio quality" (or nearly so)* | *(+1 to +10)* |
| **Maximum Possible Total Points** | **100** | |
| **Deductions** | **&darr; Don't lose points for any of these! &darr;** | |
| *Deduction if required proposal/prototypes are not submitted to dropbox on time* | *(-10 each)* | |
| *Deduction if final documentation is not submitted to dropbox on time* | *(-10)* | |


<hr>

## VI. Submission
- see myCourses for details & due date/time

<hr>

## VII. Examples

### A. *Recipe Map*

- Below is the main screen
- Clicking on the "Too Lazy" button also brings up a map of restaurants that offer the desired cuisine

![screenshot](_images/project-3-example-1.jpg)

### B. *RIT Pathfinder*

**Walking route:**

![screenshot](_images/project-3-example-2.jpg)

**Biking route:**

![screenshot](_images/project-3-example-3.jpg)



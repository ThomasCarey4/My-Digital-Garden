---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-1/intro-to-web-technologies/design-for-coursework-2/"}
---

## Additional Features
### Homepage
I plan to add a small addition to the homepage of my website that will take take advantage of HTML5’s geolocation feature to inform the user how far they are away, in metres or kilometres, from my accommodation. I also plan to use HTML5’s local storage to store a record of the closest the user has come to my accommodation, and inform the user of their record and if they break it.
### Navigation
I plan to completely revamp my current navbar and replace it with a customised Boostrap navbar. This should make my html much cleaner and allow for my next addition.
As I have a list of books I like on my site, I plan to add a Bootstrap [modal](https://getbootstrap.com/docs/5.3/components/modal/), to the navbar, that contains a html form allowing the user to recommend me books.
### My Dog Collage
I can’t think of many changes I could make to this site and so I plan to simply randomly shuffle the images of the collage using JavaScript.
### Biscuit Recipe
Similar to the dog collage, there aren’t a huge number of changes that could make this site ‘more advanced’, therefore I have decided to add a simple timer to the side of the page to allow for anyone using the recipe to time their baking without leaving the site.
### Hot Air Balloons
I plan to make this site more interactive by making the hot air balloons images spinnable.
### Books
I hope to be able to link this to my [Goodreads](https://www.goodreads.com) shelf to make it dynamically updated with any new books I add and if change my ratings.
I plan to display these books as Boostrap [cards](https://getbootstrap.com/docs/5.3/components/card/) in a grid format, ordered by rating.

---
## My Implementation
### Homepage
Using the [module’s notes](https://alt-6100e9398f586.blackboard.com/bbcswebdav/courses/202223_35262_COMP0021/site/Advhtml/) on geolocation and local storage, I was able to smoothly implement this with some help from the [Haversine Formula](https://community.esri.com/t5/coordinate-reference-systems-blog/distance-on-a-sphere-the-haversine-formula/ba-p/902128).
![Geolocation.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Intro%20to%20Web%20Technologies/images/Geolocation.png)
### Navigation
Using the Boostrap [documentation](https://getbootstrap.com/docs/5.3/components/navbar/) this was quick to set up. I decided to move from an Iframe to the jQuery load function as the Iframe proved to be more complicated.
```javascript
$('#navbar').load('navbar.html', function () {
...
```
For the book recommendation form, the html was easy to implement however finding someway for the recommendations to reach me was a challenge. My idea was to use google sheets (As I use for the list of books) however that turned out harder than expected due to CORS errors. Nevertheless, I managed to write a google apps script to allow the JavaScript to PUSH to the google sheet properly using [this forum post](https://stackoverflow.com/a/68933465/7480256) to get around CORS.
The sheet can be found [here](https://docs.google.com/spreadsheets/d/1m9gygegMBvMbbtXslAR5KyEnCwoFvTWH7uwSVNGcEfo/edit#gid=1171914841) 
### My Dog
This was also as simple task where I just shuffled an array of the images
```javascript
...
imagesArray.sort(() => Math.random() - 0.5);
...
```
### Biscuit Recipe
This one was a challenge to implement as I couldn’t find a good way to present the timer other than numbers. In the end I chose to use a Boostrap [progress bar](https://getbootstrap.com/docs/5.3/components/progress/) as it appears close to what I want.
I also changed where I display the timer to be inside a [modal](https://getbootstrap.com/docs/5.3/components/modal/) as placing it next to the text was difficult for smaller screens such as a phone to display.
![Timer.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Intro%20to%20Web%20Technologies/images/Timer.png)
### Hot Air Balloons
I successfully made the images spinnable by making it so hovering your mouse over them spins them clockwise, and clicking on them resets them.
### Books
I first tried to do this by using the Goodreads API but sadly discovered that their API shut down in 2020. As a result I had to think of a different method and decided to export my shelf as a CSV and upload it to my google drive. With this I was then able to use jQuery’s AJAX to fetch this CSV and sort it by rating.
I also found this can take a few seconds to process so I added a Boostrap [spinner](https://getbootstrap.com/docs/5.3/components/spinners/) so the user knows something is happening.

---
## My Testing
I have extensively used Firefox’s ‘Responsive Design Mode’ to check if my site displays and functions properly on a variety of screen sizes.
### Homepage
I was tested my geolocation script in a variety of locations and have discovered it to work properly and successfully save to local storage.
My homepage also looks good in small screen sizes.
### Navigation
My navbar works perfectly on small screens with a hamburger menu appearing if the screen cannot fit all the navigation options.
The modal also displays perfectly on small screens.
### My Dog
This sites successfully shuffles the images and displays properly on mobile.
### Biscuit Recipe
I have tested the timer against the clock on my phone and phone it to be accurate. I have also tested the modal and found it displays properly on mobile.
### Hot Air Balloons
There were some issues with how this displayed before but these have been rectified and the site now displays without fault on mobile.
### Books
As I am using Boostrap cards, this also displays perfectly on Firefox’s mobile screen, as it switches from a grid view to a list of cards.
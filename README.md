# Trending Stories


## Table of contents
* [General info](#general-info)
* [Intro Video](#intro-video)
* [Technologies](#technologies)
* [Setup](#setup)
* [Features](#features)
* [Status](#status)
* [Contact](#contact)
* [License](#license)


## General info
Trending Stories is a website that pulls in all the top trending news stories, and refreshes as the day goes on! You can search for stories using the built in categories; Trending, Sports, Entertainment, and Technology. For a more taylored search, use the search option to find the stories you are looking for. There is also a My Feed feature that allows you to add and remove stories to a personalized feed specific to your choices. You can use this if you are in a rush and would like to read them later, or save them there to easily reference and share  with a friend. Lastly, to make things a little easier for you, there is an auto-scroll button that allows you to see all the articles scroll through hands free!

## Intro Video

video link here. 

## Technologies
* Ruby - version 2.6.1
* Bootsnap - 1.4.2
* RestClient - 2.1.0
* SQLite3 - version 1.4
* API - Newsapi.org

## Setup
To run the site, install it locally by cloning the GitHub repository, and in your Terminal type:
```javascript
cd into the backend 
run bundle.install
run rails s 
```
``` javascript
cd into the frontend
run lite-server
``` 

## Features

* Browse the top trending stories!
* Search for specific topics using our dynamic search feature.
* Save stories to your personlized My Feed.
* Allow the site to do the work for you with our auto scroll button    
  that can be conveniently turned on and off.
    

## Code Examples

``` javascript
function carouselCards() {
    timer = setInterval(function() {
      const $parentContainer = document.querySelector('.container');
      const $divCard = $parentContainer.querySelectorAll('.item');
      $divCard.forEach((card) => {
          card.classList.toggle('sliding-now');
      })
      setTimeout(function() {
        $parentContainer.appendChild($divCard[0]);
      }, 5000);

    }, 5000);
  }
```

``` javascript
fetch(articlesURL)
    .then(response => response.json())
    .then(articles => displayStories(articles))
    .then(addingEventListeners);

function displayStories(story) {
    story.forEach(showStory)

    const loadingGif = document.querySelector('.loading')
    loadingGif.remove()
};
```


## Status
Project is finished with option to expand features and further refactor code.


## Contact
Created by [Augie Menos](https://www.linkedin.com/in/augie-menos-9b8329b1/) and [Kevin Johnson](https://www.linkedin.com/in/kevin-johnson805/)


## License

Copyright (c) [2020] [Augie Menos and Kevin Johnson]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
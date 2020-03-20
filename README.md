# LIRIbot

Welcome to LIRIbot!

This application will assist you with the following:

1. Look up a song title to reveal the artist, album title, and preview URL.
2. Search for a concert tour schedule of your favorite artist.
3. Search for your favorite movies to reveal release dates, actors, ratings, etc.
4. Enter a random search and tell LIRIbot to "Do what you say!"

## How It Works

-Open the application in your terminal or bash. Run 'Npm Install' to install axios, Spotify, and moment packages.

-For a song search simply enter 'node liri.js spotify-this-song' then the song name to pull up the information.

-To concert search, enter 'node liri.js concert-this' then the name of the band to reveal tour dates.

-To search for your favorite movie stats, enter 'node liri.js movie-this' then the movie name to view the movie information.

-For 'node liri.js do-what-it-says', open the random.txt file, tell it your command, then enter in 'do-what-it-says' to the terminal.

It's as easy as that! Enjoy LIRIbot!

Technologies used are javascript and node.js

## View examples of use here:

![Liri1](https://user-images.githubusercontent.com/53287044/74381464-bd0fdf80-4da8-11ea-8d38-85755a53f5cf.jpg)

![Liri2](https://user-images.githubusercontent.com/53287044/74381475-c00ad000-4da8-11ea-93dc-0fb25c394a07.jpg)

![Liri3](https://user-images.githubusercontent.com/53287044/74381479-c26d2a00-4da8-11ea-9aeb-6875c3e02f91.jpg)

![Liri4](https://user-images.githubusercontent.com/53287044/74381485-c5681a80-4da8-11ea-946f-b1beb8d7ac6b.jpg)

## Technologies

* Node.js
* JavaScript
* jQuery

## Behind the Scenes

Here's an example of how the code loops through the search results from Spotify:
~~~
function spotSearch(input) {
    spotify
        .search({ type: 'track', query: input })
        .then(function (response) {
            var previewUrl = response.tracks.items[0].preview_url
            var artist = response.tracks.items[0].artists[0].name
            var song = response.tracks.items[0].album.name
            console.log(`Artist: ${artist} \nAlbum:  ${song} \nPreview URL: ${previewUrl}`)
            var easy = JSON.stringify(response.tracks.items[0], null, 10)
            })
            
        // })
        .catch(function (err) {
            console.log(err);
        });

}
~~~

## Contact
Please contact me directly with any questions or comments!
* jlynnraz@gmail.com
* [LinkedIn](https://www.linkedin.com/in/jaimee-razee/)
* [Portfolio](https://jlynnraz.github.io/Portfolio2/)


---
layout: post
title:      "TOPSIX CLI GEM"
date:       2018-05-07 15:11:48 +0000
permalink:  topsix_cli_gem
---


Wow who could Have thought that I would be making a gem from **scratch!** 

I decided for my CLI Gem project to build it around something I love. Music

I wanted to scrape my favorite new music site [ PitchFork](https://pitchfork.com/best/) for the all the information required for my gem.

After figuring outwhat Kind of gem I wanted and the website it was time to think ways I can approach this. 

```
To DO:
1. Create a new gem using bundler
2. build a UI of things you want you gem to do with some face infor
3. make that information real
4. remember to save and make comment's on any changhes you submit.
5. make changes that need to be done


    --What to do I want for my CLI project about--

1. PitchFork grab the best new albums list
2. Parce that list to my gem and return the title, artist, genre of the top albums
3. get input from user to choose the album that they want the score from in a number list
4. return score with small snippet of the article.
5. The url where the albums is found to read the full review.


UI

-- Welcome to top 6 gem --
'list' for the top 6 'exit' to leave
user inputs 'list'
    top 6 albums with title, artist, and genre prints

user inputs 1-6 to pic album
    returns the album score and a quick summary of that album.
    possibly shows a link to the full review

asks for input again 'Exit' or 'List'

exits if input = exit else lists the top 6 again.

"See you next week!"
```

Essentially from the Notes above I wanted to greet the user, show the top 6 albums reviewed so far, and for the one level deep required I wanted to show the rating it received plus a quick snippet of the review.

The level deep is where it got tricky. All of these reviews had different urls I needed to figure out a way that if the user picked  "1" it would return the correct review. 

I came up with the deciscion to add an the option to takein an input in my #review_scrape method

```def self.get_review(input)```

Viola. It worked! I was getting the correct information!

Going from a terrefying empty text edditor to a couple of files with with 30-90 lines of code. ***#self.pat_in_back*** 

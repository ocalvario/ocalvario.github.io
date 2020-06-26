---
layout: post
title:      "Protein Bar CLI"
date:       2020-06-26 21:36:43 +0000
permalink:  protein_bar_cli
---


In light of the COVID-19 lockdowns forcing many to work from home, many of us are faced with daunting choices around which snacks to purchase from your local Walgreens/Duane Reed, CVS, or Rite Aid. Among the more confusing snacks are the protein bars - should I try a new bar that is heavily discounted, or is it not worth the risk. To facilitate decision making, I built a short and easy CLI using scraped data from a website with a lot of protein bar review data - [LabDoor](https://labdoor.com/rankings/protein-bars). 

The first challenge was figuring out the right flow for the program. Many pieces of data are available at various locations, so I tried to focus on the elements that were the most scrape-friendly in terms of their structure. It took a bit of trial and error to figure out the optimal structure.

Of immense help were the various CLI Live Project Build by Beth Schofield. Being able to stop and recreate each of her steps, ensuring I was working through the same erros was extremely helpful. Would highly recommend that others starting this project do the same. The problem arose though when the final video was not online! Luckily, I was able to find the github repository and could then (albeit slowly) work through the steps for the finishing touches.

Having the CLI structure in place, I was able to try a number of different potential variable structures for the scrape. Ultimately, I settled on a two step process where the links were scraped from the index page, which were then used to initialize the Bar class with a url. Then, there were subsequent scrapes to get the other attributes. Figuring out how to populate the empty parameters with scrape data took some trial an error, but the example code went a long way towards figuring it out. 

Once the main structure was working, I then had to put some improvements - i.e. the initial list was by order of raitings, so I re-sorted alphabetically to be more user friendly. I also made a fair amount of formatting changes to make it easier to read.

The only other advice I would share is in testing out your scraping especially, I would make use of Repl.it in terms of seeing if different sections are working. Having that resource to test and figure out the parts of the scrapes made putting it all together that much easier.

Good luck to all staring upon this project! 

Just as a starting note: I ended up downloading text wrangler because previously I was using atom which was crashing over and over again during the exercises. I'm not sure if anyone else had this issue but it was quite annoying so hopefully this one works better!

So, first things first, I copied the full text into Text Wrangler, and then saved. Then I deleted all the irrelevant information until I had just the instructions. I scrolled through the document deleting any large chunks of information that didn't look like a letter. 

![first-image](https://www.dropbox.com/s/3athgiiuosb3hm6/%286%29.png?raw=1)

Then, clicked find all, and using the correct query for TextWrangler, I replaced/added a "~" in front of all of the lines. 

![second-image](https://www.dropbox.com/s/fpi6hfpl2wezqqo/%287%29.png?raw=1)

Then I went into RegExr to see if it worked correctly, which I think it did. Then, I needed to get rid of all the extra stuff that I may of missed previously. Just like the instructions of the workbooks said, by finding all the beginings that do not have ~, and then replace it with nothing, effectively I'm left with just the series of letters. When I replaced it, it worked perfectly, cutting the document by 98 lines. 

![third-image](https://www.dropbox.com/s/hpuwdl1564q9d7l/%288%29.png?raw=1)

 Next, I deleted all of the uncessary extra lines. I did this by replacing the blank space with nothing.
 
Going into regex, I put in the text and then this: [0-9]{4}.+ -- which seemed to highlight the date and the page number. Then, I went back to my text editor. I thought really hard about this, and if this was the entire last half: (,)( [0-9]{4})(.+), then if we replace with [0-9]{4}, it should get rid of the page numbers for all the lines. 
So instead of the year, and then the page number, we would be left with just the date. 

So that didn't work, because it got rid of everything. 
![fourth-image](https://www.dropbox.com/s/y322ucxrd02rai9/%289%29.png?raw=1)

Thank god command-z worked, because honestly hadn't been making as many saves as I should've. But back at it: I kept trying to delete the first and the last but for some reason it physically changed the date to the code. 

I realized that I was on the right track, but not quite there. Then I went back and read over the introduction. I needed to think of this as groups. 
(,)( [0-9]{4})(.+)
(,) - \1 , or group 1
([0-9]{4}) - \2 or group 2
(.+) - \3 or group 3

With that in mind, then all I needed to put as the query in the replace was \2! because that is the only one I want to keep. 

Tada! It worked. God, this working felt so awesome. 
![fifth-image](https://www.dropbox.com/s/5agzhzp25lm75p1/%2810%29.png?raw=1)

Just as a little cheat, here's what it looks like: 
![sixth-image](https://www.dropbox.com/s/uovjb9src8tveht/%2811%29.png?raw=1)


Then, to get rid of the tildes, all you need to do is this: 
![seventh-image](https://www.dropbox.com/s/v4lwtw0yjgz0rz3/%2812%29.png?raw=1)

Replace all and then all the tildes will be gone. 




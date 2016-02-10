I'm finally writing up my experiences with Module 2 exercise three. 


GETTING STARTED 
First things first, I searched up "ottawa" w/ the date range 1800-1900, and then entered it into the Canadiana Discovery Portal. After that, I noticed the search query in the url as I was supposed to, and put in:
&fmt=json
Once I did this, the data looked much, much different -- it makes sense that this is what really works for machines compared to what we see designed to look visually appealing. 

Alright, so after that, I didn't have wget after testing in terminal, so I used the instructions and ended up installing Xcode. (took a lifetime though, almost 5g to download! plus installing time )

On Ian Milligan's instruction guide he said that I would have to install the Command LIne Tools kit in Xcode, however in new versions of OS X turns out you don't need to(after some googling I found this out) -- it's already automatically installed. 

Then I went to Homebrew and got this installed through my terminal. I then installed wget :) 

Next, I needed to download this file: api-ex-mac.sh

So, I used the guide from programming historian .org once again, and followed this in detail. I decided to use the tutorial first and made a folder named "active-histories" and downloaded a few pages onto my computer, worked like a charm, and extremely fast. 

DOWNLOADING THE SCRIPT
After doing that, I tried to download the api-ex-mac.sh but I realized I wasn't in the correct repository. Went to slack and realized I was supposed to just grab and save from the class git hub! So after doing this, I tried to change the file a bit so that I could use the script for its purpose! Really I was just tinkering around but at first I changed the date to 1890-1900 and place to Ottawa (both links starting with "curl".)

I had a couple of errors, firstly I needed to command using sudo chmod 700 to basically "tell" my mac to run the script. 

But I was using Xcode(weirdly) as a text editor so things weren't working well. A bunch of extra stuff got added at the top of the script so this made it so that nothing worked. 

Then, when I tried to use Atom, I realized I had somehow managed to make it in a weird phone-like setting. Not even kidding, check that out: 

So Dr. Graham helped me in resetting this so that I was back to normal text editing mode(thankfully!!)

Then, finally to running the script. So like I said, I changed the date range to 1890-1900 and then the place/search query to Ottawa, and then ran the program that I named "ottawa.sh". 

Then, I ran into more and more problems. Terminal continously ran for a reaaaally long time, doing something-- I have no idea what. So, I went back to the original script and ran that, and it worked as it should: 

Then, I went back to my script I had created (named ottawa.sh). Turns out I had a discrepancy between the two links and once I fixed that: bam, it worked! such a good feeling to have this working... you have no idea.

Quite honestly, I'm exhausted so I'm going to call it a night and try the splitting tomorrow. 	


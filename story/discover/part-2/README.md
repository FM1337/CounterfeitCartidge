# How I discovered this cart was a “counterfeit” Part 2
## NOTE
If you haven't read part 1 yet, I strongly recommend you read it before reading this part, it will make a lot more sense.
[Click here](https://fm1337.github.io/CounterfeitCartidge/story/discover/part-1/) to read part 1!

---
After my testing had concluded, there wasn't really many updates made to the research. I was busy with school and there wasn't
really anyone else that was having this issue that I could ask to continue testing, and by now the grace period for returning
the cart on Amazon and getting a refund or an exchange was long gone.

But I finished the winter semester, had a week off before my work term started and I was bored, so I decided to pick this up once again.

At this point, I was still operating under the assumpition that if the CRC32 Checksum was different from the ROM dump on the internet, then the card was a counterfeit.

I decided to redump the cart again, but this time grab the trimmed version along with the non-trimmed version and check the CRC32s from the internet ROM and this was the result:

![test](https://i.imgur.com/tsWrvgR.png)
(Note the red boxes means the information doesn't match, green means it does match, and blue is just information)

I wrote a bit up about the situation on discord as seen on this screenshot
![discord screenshot](https://i.imgur.com/iOLCZG2.png)

```
bit concerning when the CRC32 doesn't match
I mean I understand the trimmed version wouldn't match
but the non-trimmed versions of the same revision and same country should have the same CRC32
I can't find any references to my cart's crc32 version online
while I have found references to the pirated version
which leads me to believe one of three things
1. My cart is a counterfeit
2. Every cart's ROM has a different CRC32
3. The revision or country of my ROM is incorrect
1 and 3 would probably tie together
and 2 is unlikely as hell
This wouldn't be a problem if save exporters wouldn't freak out on my cart, 
but everytime I try, they either crash the console, or export a 0 byte save. 
and The one that exports the 0 byte save cannot restore any saves I bring in either
```

For some reason I was dead set on number 2 being wrong, I was proved wrong in the next few minutes by a user named TrainBoy2019 on discord who was kind enough to dump his Pokemon diamond cartridge, here are screenshots
### Non-Trimmed
![non-trimmed](https://i.imgur.com/ztRS1hd.png)
### Trimmed
![trimmed](https://i.imgur.com/cpLW24G.png))
I quickly updated my earlier graphic showing off the new information discovered 

![result](https://i.imgur.com/2D2Ic0O.png)
(sorry for the low quality picture, I lost the original copy)

Then another kind user came along and dumped their Pokemon Diamond cartridge as well and here are the results for his dump
### Non-Trimmed
![non-trimmed](https://i.imgur.com/ns1XBTu.png)
### Trimmed
![trimmed](https://i.imgur.com/KmVpvny.png)

Right off the bat with these dumps you'll notice something interesting, while the CRC32 of the non-trimmed roms don't seem to match, the CRC32 of the trimmed ROMS do match. Both trimmed ROMs have a CRC32 of **F3B5338E** this meant that all ROMs of the game from the same region and revision will most likely have a different CRC32 if they aren't trimmed.

Griffin and Train both confirmed their carts were legit, Griffin had got his copy of the game in 2007 and Train got his between 2011 and 2013.

At this point, the creator of CheckPoint [bernardogiordano](https://github.com/bernardogiordano) chimes in with a bit of information/a suggestion
```
I think that the SPI functions we use in Checkpoint and TWLSaveTool don't know what to do with your cart
Check with FBI just to see
```

So I decided to try his suggestion, and the results weren't pretty, I recorded a YouTube video with the results which you can see by clicking the image below

[![Video Thumbnail](http://img.youtube.com/vi/eCPS31rFThk/0.jpg)](http://www.youtube.com/watch?v=eCPS31rFThk)

And that my friends, is pretty much the conclusion of this story, there's no real happy ending to it just yet, I haven't found any thing that works so far but I'm not giving up. If you wanna see what I've tried so far you can do that by clicking ~~here~~ (Coming soon).

Thanks for reading the story up till now and I hope in the future we'll find a solution.

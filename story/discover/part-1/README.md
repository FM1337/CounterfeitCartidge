# How I discovered this cart was a "counterfeit" Part 1
(Side note if you haven't read the first part, you can do so by [clicking here](https://fm1337.github.io/CounterfeitCartidge/story/obtain/
))

So, quoting one area in the previous part of the story
```
I got home booted it up and it worked fine. I could save and play the game without any issues that I could see.
```

This part still remains true, there isn't any issues with playing through the game like normal:
- Saving works fine
- Gameplay is normal with no issues
- The cartridge is reconized like a legit copy of Pokemon Diamond
- The cartidge itself doesn't show any signs of being a counterfeit/bootleg

If there were no issues with the game itself at all, why am I calling it a counterfeit?

Well, it's because I discovered issues with interacting with the cart because of lazyness. See I didn't want to have to play
through Pokemon again just to transfer over Pokemon to the pokebank so I decided to try importing a save file from the internet
onto the cartidge.

My first go to solution was [CheckPoint](https://github.com/BernardoGiordano/Checkpoint) a save manager utiliary created by bernardogiordano

So, I grabbed a save file from GameFAQs, used the Shunyweb save converter, and "injected" the save file onto the cartidge.
I booted up the game and... nothing, the old save file was still on the cart and nothing had changed.

Having found this to be odd, I attempted to export the save file from the cartidge to the sd card on my 2DS, and while it appeared to export the save file, in reality it had failed and just created a 0 byte file.

As CheckPoint not working, I decided to give [TWLSaveTool](https://github.com/TuxSH/TWLSaveTool) a go. The only problem was, when I attempted to boot it up with the cartidge in the slot, this would happen:
![TWLSaveTool Crash](https://i.imgur.com/tSp3X62.png

With both CheckPoint and TWLSaveTool not working, I began to ask around and that's when I started talking with a user named ❅FrozenFire❆ on discord.

We talked back and forth about the situation and I was asked if I could dump the ROM from the cartidge and get the header information about it. I dumped it and here was the information I got from the ROM
```
----------------------------------------
Header Info for: POKEMON_D_ADAE01_05.nds
----------------------------------------
Internal Name   : POKEMON D
Game Serial     : NTR-ADAE-USA
Maker Code      : 01
Publisher       : Nintendo
Version         : 1.5 (05h)
Secure Checksum : 6575 (BAD)
Logo Checksum   : CF56 (OK)
Header Checksum : CA37 (OK)
File Size       : 512Mbit (67108864 bytes)
Card Size       : 512Mbit (67108864 bytes) (09h)
File CRC32      : 94980279
----------------------------------------

----------
Language 1
----------

Pokémon Diamond
Nintendo

----------
Language 2
----------

Pokémon Diamond
Nintendo

----------
Language 3
----------

Pokémon Diamond
Nintendo

----------
Language 4
----------

Pokémon Diamond
Nintendo

----------
Language 5
----------

Pokémon Diamond
Nintendo

----------
Language 6
----------

Pokémon Diamond
Nintendo
```

![Screenshot with information](https://i.imgur.com/eHhMHE4.png)

Frozen decided to grab the information from a well known dump of the game and the CRC32 was different between both ROMs.

![Another screenshot with information](https://i.imgur.com/KmQO6Dd.png)

At this point Frozen was out of ideas, after suggesting an idea to use the flash cart to grab the save and then upload it to the PC via ftp (which wouldn't work because the NDS only supports WEP), we had decided to take a break from trying to figure the problem out, I thanked frozen and for a few months, that was all there was to it.

To view the next part ~~click here~~ Coming Soon

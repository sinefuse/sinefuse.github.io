---
layout: post
title: Polling rates on keyboards and why they matter
---

I feel like I see this pop up quite often. People tend to want keyboards with 1000Hz polling rates in custom keyboard communities, and then people just shrug it off, usually with a response such as "That is ridiculous, you do not ever need 1000Hz because of debounce and you can't even react that fast for you to matter, etc etc."

While from a theoretical standpoint they would be correct, practically, it couldn't be further away from the truth. Allow me to explain why, using rhythm games as an example.

Rhythm games are a genre of game where you press notes that appear on the screen, in accordance to the music you play. Depending on how accurately to the song you hit the note, you get judged by the game on how precise you are. I will use Stepmania as an example here:

Stepmania polls inputs as quickly as it can, preferably at 1000 times per second, aka 1000Hz polling (that is, if you can get the game to run that quickly, which is very possible with the most recent builds in the "Outfox" branch, where I'm able to hit over 3000fps ingame if I don't cap the framerates). If you hit a note with an accuracy of +/-22.5ms, it will be graded as "flawless", the best possible judgement. If you hit more loosely, you will get worse judgements, such as "Perfect", "Great", and worse, which will break your combo. As such, you want to try your best to stay in the accuracy range of the 3 previously mentioned judgements.

Now, this is the part where we bring in polling rate. Generally, most custom, non-gamer oriented keyboards will come with polling rates of 125Hz or 250Hz. There's many excuses as to why, such as "The internal controller can't handle faster polling rates", "It's not necessary (refer to reasons mentioned further up)" and many more. We'll use 125Hz as example and compare it against 1000Hz.

So if you use a 125Hz keyboard, this means that it will be polled for inputs only an 8th of the amount that Stepmania polls for inputs, which, as you can imagine, causes quite a large difference. This means that even if you theoretically hit perfectly at all times, there is a large chance that you will have an accuracy divergence of ~8ms, even if you hit the absolute perfect timing on every single note.

Since nobody is perfect after all, there will obviously be a bit of divergence in your accuracy - If you can hit just barely everything in the 22.5ms window of the Flawless judgement window using a 1000hz keyboard, this means that if you used a 125Hz keyboard, you will have an extra divergence of up to 8 more ms, which means that some of your keytaps might very well drop into the "Perfect" judgement, which means your Flawless Full Combo run is dead and it wasn't even your own fault. Another example is you're a newer player going for a "normal" Full Combo on a song and hit quite a bunch of notes as greats - if you use the 125Hz keyboard, there is a pretty large chance you might end up having one of the hits drop below what the game considers a "Great", which means your Full Combo run is dead.

### Pretty frustrating, as you can imagine.

With a 1000Hz keyboard, this does not happen (that is, if you have USB polling set up properly, which is generally the case on Windows and newer computers in general nowadays). Somewhat related to USB polling, I've seen people claim that gaming keyboards use two USB plugs to enable N-Key Rollover and 1000Hz. That's very wrong, generally the second USB plug is for passthrough. USB keyboards enable NKRO by installing a second USB driver to Windows. Polling rate will be fine on 1000Hz keyboards even if just one driver is installed (Yes, N-Key Rollover is decoupled from polling rate).

With this being said: The claims of debounce and what not are fair enough - for most people playing FPS and what not, the higher polling rate will not have a very big difference. However, there *is* a difference, and claiming this different doesn't exist is just plain ignorant and annoying. If someone wants a 1000Hz keyboard or wants to know how to enable 1000Hz in QMK firmware, just fucking tell them what keyboard to get or how to enable it, don't scramble around for reasons to not to do so.

Hopefully this short document was informative enough to read and gave you a bit more of knowledge on the wonderous worlds of keyboards. Share this with anyone who thinks polling rate doesn't matter and then point and laugh at them.

`- sinefuse`

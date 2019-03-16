Here are some resources for the [LÖVR open source library](https://lovr.org/) for VR games. LÖVR was created by Bjorn Swenson. These resources were created by [Mermaid Heavy Industries](https://mermaid.industries/) (that's me).

If you have questions about anything on this page, feel free to join the [LÖVR slack](https://lovr.org/slack) and talk to "mcc" (that's me). I would be curious to hear any feedback or problems you have.

# LÖDR

I wrote a program called Lodr. Lodr is a loader for lovr. Lodr will watch your Lovr program on disk while it runs, and if any of the files change, your game will reboot. This is nice because you don't have to close and reopen the game a whole bunch. Lodr is built into the LovrTest app for Android (see below), but you can use it on desktop, too, by following the [instructions here](https://github.com/mcclure/lodr).

# lovr-ent

I have a set of support files I put in every one of my LÖVR projects: An entity tree library, a 2D UI library, a namespace extension for Lua. I bundled up all my support files and posted them as a [sample project](https://github.com/mcclure/lovr-ent) you can just clone.

# Oculus Mobile support

I maintain the port of LÖVR to Oculus Mobile (Oculus Go and Samsung Gear VR). Using the port requires a wrapper app. Here's some simple instructions for quickly writing small Lua games and testing them in your mobile headset:

* You will need an [Oculus Go](https://www.oculus.com/go/). (On the Gear VR, sideloading does not seem to be possible because the signing requirements are tighter.)
* Download the most recent LovrTest.apk from [here](https://github.com/mcclure/lovr-oculus-mobile/releases/).
* Install adb and "sideload" the Test App. [There are instructions on how to do that here.](https://headjack.io/tutorial/sideload-install-app-apk-oculus-go/)
* Make a LÖVR app. A LÖVR game is a directory full of Lua files and resources. To get started you could clone lovr-ent linked above, or you could download one of the official examples (go [here](https://github.com/bjornbytes/lovr-docs), click Download->Download Zip, and look in the "examples" folder-- I like the "Physics" example).
* Once you've put together an app, cd to its directory and run exactly this:

        adb push --sync . /sdcard/Android/data/org.lovr.test/files

* On your Oculus Go, go to Library, click "Unknown Sources" (if this is not there, make sure your Go is in Developer Mode), and click "LovrTest (org.lovr.test)".
* The game you `adb push`ed will be running now. You can `adb push` again to upload a different game (if the game is running when you push, it will automatically restart).

If you want to go beyond testing and release a game with Lövr, or run on the Gear VR, you currently need to build the wrapper Android app yourself. [You can find the source and build instructions for the wrapper app here](https://github.com/mcclure/lovr-oculus-mobile).


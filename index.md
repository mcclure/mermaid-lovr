Here are some resources for the [LÖVR open source library](https://lovr.org/) for VR games, maintained by [Mermaid Heavy Industries](https://mermaid.industries/) (that's me). If you have questions about anything here, feel free to join the [LÖVR slack](https://ifyouwannabemylovr.slack.com) and talk to "mcc" (that's me).

# LÖDR

I wrote a program called Lodr. Lodr is a loader for lovr. Lodr will watch your Lovr program on disk while it runs, and if any of the files change, your game will reboot. This is nice because you don't have to close and reopen the game a whole bunch. Lodr is built into the LovrTest app for Android (see below), but you can use it on desktop, too, by following the [instructions here](https://github.com/mcclure/lodr).

# Oculus Mobile support

We have recently added support for Oculus Mobile (Oculus Go and Samsung Gear VR) to LÖVR. Using this requires a wrapper app. Here's some simple instructions for quickly writing small Lua games and testing them in your mobile headset:

* You will need an [Oculus Go](https://www.oculus.com/go/). (If you have something else, like a Gear VR-- talk to me, I need testers!)
* Download the most recent LovrTest.apk from [here](https://github.com/mcclure/lovr-oculus-mobile/releases/).
* Install adb and "sideload" the Test App. [There are instructions on how to do that here.](https://headjack.io/tutorial/sideload-install-app-apk-oculus-go/)
* Make a LÖVR app! A LÖVR game is a directory full of Lua files and resources. An easy way to get started is to download the official examples; go [here](https://github.com/bjornbytes/lovr-docs), click Download->Download Zip, and look in the "examples" folder. I like the "Physics" example.
* Once you've picked out an app, cd to the directory and run exactly this:

        adb push --sync . /sdcard/Android/data/org.lovr.test/files

* On your Oculus Go, go to Library, click "Unknown Sources" (if this is not there, make sure your Go is in Developer Mode), and click "LovrTest (org.lovr.test)".
* The game you `adb push`ed will be running now. You can `adb push` again to upload a different game (if the game is running when you push, it will automatically restart).

If you want to go beyond testing and release a game with Lövr, you currently need to build the wrapper Android app yourself. [You can find the source and build instructions for the wrapper app here](https://github.com/mcclure/lovr-oculus-mobile).

This is all brand new, so I would be curious to hear any feedback or problems you have with this!

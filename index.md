Here are some resources for the [LÖVR open source library](https://lovr.org/) for VR games. LÖVR was created by Bjorn Swenson. These resources were created by [Mermaid Heavy Industries](https://mermaid.industries/) (that's me).

If you have questions about anything on this page, feel free to join the [LÖVR slack](https://lovr.org/slack) and talk to "mcc" (that's me). I would be curious to hear any feedback or problems you have.

# LÖDR

I wrote a program called Lodr. Lodr is a loader for lovr. Lodr will watch your Lovr program on disk while it runs, and if any of the files change, your game will reboot. This is nice because you don't have to close and reopen the game a whole bunch. Lodr is built into the LovrTest app for Android (see below), but you can use it on desktop, too, by following the [instructions here](https://github.com/mcclure/lodr).

# lovr-ent

I have a set of support files I put in every one of my LÖVR projects: An entity tree library; a 2D UI library; a namespace extension for Lua; and a standalone 3D model viewer with the ability to inspect animations, skeleton nodes and materials. I bundled up all my support files and posted them as a [sample project](https://github.com/mcclure/lovr-ent) you can just clone.

# Oculus Mobile support

I maintain the port of LÖVR to Oculus Mobile (Oculus Quest, Oculus Go and with some fiddling Samsung Gear VR should work). Using the port requires a wrapper app. Some simple instructions on getting up and running are now part of the LÖVR documentation; see <a href="https://lovr.org/docs/Getting_Started_(Android)">here</a>.

If you want to go beyond testing and release a game with Lövr, or run on the Gear VR, you currently need to build the wrapper Android app yourself. [You can find the source and build instructions for the wrapper app here](https://github.com/mcclure/lovr-oculus-mobile).


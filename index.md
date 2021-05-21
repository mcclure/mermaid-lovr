Here are some resources for the [LÖVR open source library](https://lovr.org/) for VR games. LÖVR was created by Bjorn Swenson. These resources were created by [Mermaid Heavy Industries](https://mermaid.industries/) (that's me).

If you have questions about anything on this page, feel free to join the [LÖVR slack](https://lovr.org/slack) and talk to "mcc" (that's me). I would be curious to hear any feedback or problems you have.

# LÖDR

I wrote a program called Lodr. Lodr is a loader for lovr. Lodr will watch your Lovr program on disk while it runs, and if any of the files change, your game will reboot. On Desktop, these days it's more useful to hit F5. On Android however this is super useful because you can just run `adb push --sync` and the game code will update and relaunch instantly without you having to close and reopen the program.

You can find the Android and desktop [instructions here](https://github.com/mcclure/lodr).

# lovr-ent

I have a set of support files I put in every one of my LÖVR projects: An entity tree library; a 2D UI library; a namespace extension for Lua; some helpers for communicating between threads; and a standalone 3D model viewer with the ability to inspect animations, skeleton nodes and materials. I bundled up all my support files and posted them as a [sample project](https://github.com/mcclure/lovr-ent) you can just clone.

**Note:** The version of lovr-ent in the repository does not correctly support Lovr 0.15. You can find a beta of the next lovr-ent, with 0.15 support as well as a 3D/VR version of the UI library, in [my fork of LÖVR](https://github.com/mcclure/lovr/tree/andi), in the folder `game/lua`.

# LÖVR MIDI?

I have [an experimental branch of LÖVR with support for MIDI and realtime audio synthesis](https://github.com/mcclure/lovr/tree/ZP_midi). The branch comes with several small MIDI/audio toy applets. See the README and `contents.txt` files.

# ROVR

I also have [an experimental reimplementation of LÖVR in Rust](https://github.com/mcclure/rovr). I did this primarily to learn Rust. It is in a VERY primitive state but currently can launch a LOVR-style app and `lovr.load` and `lovr.update` get called as appropriate.

# Oculus Mobile support (old version)

**For historical reasons only:** I used to maintain the port of LÖVR to Oculus Mobile (Oculus Quest), which used to work via a wrapper app separate from LÖVR. Now the Android support has been folded into core LÖVR. You can still find my wrapper app [here](https://github.com/mcclure/lovr-oculus-mobile), but it will require modifications to run anything newer than the early beta of 0.14 in the git module. You may find this older version useful if for some reason you **must** build your app with Gradle. However, I recommend using <a href="https://lovr.org/docs/Getting_Started_(Android)">the normal Android support.</a>.

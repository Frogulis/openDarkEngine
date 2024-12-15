# Note to the reader
This is a fork of the main OPDE repo with no intention of merging back.
If you want the primary source code for OPDE, go look at that.

This is a fork which I have been hacking on for the purpose of rendering maps and "dollhouse" views of the first two Thief games.
If that's something you're interested in seeing, you can check it out [on my website](https://frogulis.net/thief-dollhouse/).

If you want to run this... good luck. I don't really remember what I've done, but if you're on Linux I suspect you will need to:
- compile OGRE
- fiddle around with cmake
- possibly rename a HEAP of game files to handle case sensitivity
- ???

If you're on windows, maybe it'll just work.
I get the impression the original developer was using Windows.

The main changes I've made are:
- change to orthographic view
- render the entire map at once
- extra controls

These controls are:
- Space and X to move the camera along its local Y axis (up and down)
- Q and E to roll the camera 90 degrees counter-clockwise and clockwise
- F, G, H, V, B, N to set the camera to the 6 "cardinal" directions

The changes I've made to the code in order to do this were not made with any consideration for others or for the future.
Have fun! :D

# openDarkEngine

This is a readme file for the openDarkEngine project.

openDarkEngine (OPDE) was created as an effort to build a multiplatform engine supporting the LookingGlass'es (TM) data files from the original DarkEngine(TM) games. So far, a basic display of the levels work, including objects and (broken) lighting. 

Efforts were previously started to bring in simulation code and scripting support, but after a long hiatus this project is now undergoing a *refactoring/cleanup* phase, that will continue with removal of Ogre3d library and dependencies, to be replaced with a thin, rendering only library (f.ex. bgfx). This means resource/scene management will have to be written. Bulky python script bindings will probably get replaced with a more manageable Squirrel language bindings. 

The plan is to clean up the project, and bring it up-to-date before continuing with efforts to develop things further. Main limitation right now is usage of Ogre3d, which is more designed towards new content creation than to bring an existing game engine with different design to life. With coming time, this disparity will only grow.

## License
All the files, if not specified otherwise, are released under the GNU/GPL license.

## Building
There is some partially obsolete info with build instructions in the doc/DEVELOPERS file. This will be updated after the project cleanup is finished, which includes a transition to another rendering library.

## Help needed
This project would obviously benefit from more developers. Anyone willing to participate is welcome, please start by diving in the project, look at some issues that are in the tracker, maybe try fixing something or improving something.

## Thanks

Thanks go to:

* TomNHarris (telliamed) - for the all the work he has done understanding the Dark Engine and its data formats. Also for the irreplaceable help in the past.
* ShadowSpawn - For the BIN mesh format and Movement database format descriptions.
* ataricom - For helping out with the (now defunct) sourceforge Wiki
* TTLG community
* ...and others not mentioned

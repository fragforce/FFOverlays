# FFOverlays
Graphics, Videos, and OBS configurations for Fragforce's Streams

## TL;DR - OBS Studio - Windows
* Install the 64 bit version of VLC from [HERE](https://www.videolan.org/vlc/download-windows.html) if you don't have it. 
* Download [the full repo zip](https://github.com/fragforce/FFOverlays/archive/master.zip)
* Extract the overlays folder to C:\Stream on Windows
* Copy any EL/CMN videos you want to use for commercials in the C:\Stream\overlays\Commercials folder
* Import the OBS_Overlay.json file into OBS (Scene Collection -> Import)

## TL;DR - StreamLabs OBS
* Install the 64 bit version of VLC from [HERE](https://www.videolan.org/vlc/download-windows.html) if you don't have it. 
* Grab [the main overlay file](FragforceOverlay.overlay) from here
* Import it using OBS by going to options and then Scene Collections
* Go to the Commercials scene and edit the playlist in the 'Commercial Player' Source to point to the folder where your EL/CMN videos are.

## TL;DR - OBS Linux
* What are you even doing reading this?  If you know Linux, you dont need my help, go do your thing!

## About this github
This is where you can find all the basic images Fragforce participants can use in their OBS stream layout to help standarize stream branding.

## Color Palette
* #4E738B
* #7A9DB6
* #30292F
* #223843
* #3F4045

## Content Summary
There are five complete gaming layout pages:
```
OverlayBarBottomOnly 	
	White bar along the bottom of the screen, 
	standard logo in the bottom left corner,
	designed to have game overlay completely 
	fill the screen and be partially hidden behind the bar.

OverlayBarsSmall
	White bar along the bottom and left side 
	of the screen, standard logo in the bottom 
	left corner, designed to have game overlay 
	fit to the space while not being hidden by the bar.

OverlayBarsLarge
	White bars along the bottom and left of 
	the screen, Larger logo on the left side
	above the title.  The white bars take up 
	(approximately) 20% of the space, allowing
	user to add text and webcam to the area 
	without overlaying above game overlay space.

SplitSetup
	Specially Designed space designed for split 
	camera or non-game focused uses, i.e. IRL 
	space with Twitch Chat, or two camera space.  
	Semi-transparent logo in bottom right corner
	recommended.

CamAndLogo
	No bars are used -- only the webcam box and
	a semi-transparent logo are overlaid.
```

There are also two non-gaming scenes included:
```
SpinningLogo
	Simply the Fragforce animated spinning logo in a video file,
	best used as a quick intersitial

Commercial
	Layout with a VLC source player, designed to
	be used as a 'commercial break' where you can
	play videos from your charity while preparing
	more events/games and such, or while taking a
	break.
```

And finally, three other support scenes are included:
```
Alerts/Overlays
	This scene is the overlay that should go over all
	scenes.  It includes Fragbot integrations and should
	be at the very top of all other used scenes.  The
	layout defaults at 1080p and should stretch over
	the entire screen to work properly.

Offline
	Simply the offline image.  Don't have this on
	for more than a few moments, as that just looks
	bad for everyone XD

Framed Webcam
	This is the scene that has the default webcam
	you are using for facecam, and a border.  If you
	need to change the webcam source, or replace it
	with something like facerig, change that here
	and it will be replaced on all other scenes.

```

## Theme Requirements
Transparent animataed logos are being used in all scenes, and are encoded using VP8.  Issues can be most often resolved by updating your version of VLC, though please file an issue or reach out to us on our [Discord Server](http://discord.fragforce.org) if you have any problems.  Alternatively, you can use the static png logo included in this repository to reduce processing overhead and size.

## Color Palette
Fragforce now has a general color palette, based on the logo and some shuffling.  The colors we have used in this layout are:
- #4e738b
- #7a9db6
- #30292f
- #223843
- #3f4045

## A note on the logo
After speaking to someone who does this for a living, it has been recommended that we follow these rules in relation to the logo:
- There should always be a padding of at least 1/16th of the size of the logo on each side of the logo from any edge, any other specific piece of art, or the edge of any intentionally created container
- Only put it in areas that are not \'busy\', that is, visually noisy.  if you have a colorful background behind it, or it will significantly overlay on the game background, use the transparent logo.
- Though the logo can crop over other items on the display, per the rules above, the logo itself should never be cropped.

## TODO List
- [ ] Add themed widgets
- [ ] Change Individual Charity Logos to maybe animated rotating single logo?

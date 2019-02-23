# FFOverlays
Graphics, Videos, and OBS configurations for Fragforce's Streams

## TL;DR - OBS Studio - Windows
* Download [the zip](https://github.com/fragforce/FFOverlays/archive/master.zip)
* Extract the overlays folder to C:\Stream on Windows
* Import the OBS_Overlay.json file into OBS (Scene Collection -> Import)

## TL;DR - StreamLabs OBS
Grab [the main overlay file](FragforceOverlay.overlay) from here, and import it using your OBS to get all the associated overlays!

## About this github
This is where you can find all the basic images Fragforce participants can use in their OBS stream layout to help standarize stream branding.

## Color Palette
* #4E738B
* #7A9DB6
* #30292F
* #223843
* #3F4045

## Content Summary
There are four complete gaming layout pages:
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
```
A fifth minimal layout can be used by simply using no bars, and adding the semi-transparent logo to a corner of the screen.

## Other File Includes
An offline logo png and a stream standby loop video are included in the content, which can each be used on their own as a offline image and as a standby animation.  You will also find a simple rectangle overlay in this repository, this can be used as a border around any widescreen item, including webcams or widgets, to give a neater feel to any inserted pieces.

## Theme Requirements
The transparent animated logos used in the layouts must be uncompressed AVI files (as they use png transparency) and as such are larger files.  These files are now small enough to be stored in the repository, and you will find them in the Overlays folder.  Alternatively, you can use the static png logo included in this repository to reduce processing overhead and size.

## Color Palette
Fragforce has a general color palette, based on the logo and some shuffling.  The colors we have used in this layout are:
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
- [x] Rework split screen layout (maybe darken or change colors)


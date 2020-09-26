# FFOverlays
Graphics, Videos, and OBS configurations for Fragforce's Streams

## TL;DR - OBS Studio - Windows
* Install the 64 bit version of VLC from [HERE](https://www.videolan.org/vlc/download-windows.html) if you don't have it. 
* Download [the full repo zip](https://github.com/fragforce/FFOverlays/archive/master.zip)
* Extract the overlays folder to C:\stream on Windows
* Install the fonts from the Fonts Folder onto your system
* Copy any EL/CMN videos you want to use for commercials in the C:\stream\videos/commercials folder
* Import the FF2020_Proper.json file into OBS (Scene Collection -> Import)
* Go change the specifics on in your configuration to point to your specific Extra Life account (see Configurable Content below)

## TL;DR - StreamLabs OBS - Temporarily deprecated, please use OBS official

## TL;DR - OBS Linux - Out of date, please nag at pArkervcp to Fix this
* To make it easier for linux users we have added a linux specific overlay file.
* Install your linux flavor of VLC
* The linux overlay requires that you install [obs-linuxbrowser](https://github.com/bazukas/obs-linuxbrowser/) plugin. It's super easy to do.
    * The audio will play over your default desktop audio device due to the way chromium works on linux.
* Download the repo zip and unpack, or `git clone` it, to `/stream/`
* Import the `OBS_Overlay-linux.json` into OBS under the `Scene Collection` menu item.
* Go change the specifics on in your configuration to point to your specific Extra Life account (see Configurable Content below)

## About this github
This is where you can find all the basic images Fragforce participants can use in their OBS stream layout to help standarize stream branding.

## Color Palette
Fragforce now has a general color palette, based on the logo and some shuffling.  The colors we have used in this layout are:
* #4E738B
* #5C2751
* #F09B00

## Streamable Content
The scene list is split into three different sections separated by a list of dashes in the scene list.  The first section is the group of usable visible scenes:

### About_To_Go_Live
	All streams should likely start here.

### Countdown_Intro
	This scene is a playlist of videos that can
	start the beginning of your stream, starting
	with a countdown timer, then the intro video
	and a few loops of the logo.  you will need to
	transition into your next scene manually during
	the logo loops to prevent stalling.

### Intro_Chat_One_Camera
	This scene shows your webcam along with some basic
	donation info and the twitch chat.  This can be your
	audience engagement screen, and is good to keep
	conversations logged in the VOD for future reference.

### Widescreen_Game_Layout
 You're probably going to use this the most, if you're not playing retro games that force you to use a 4:3 layout

### Retro_Game_Layout
	A gaming scene where the game you are playing is 
	traditional 'old school' TV aspect ratio, good
	for retro or some indie games.

### BRB
This is a simple static screen that you can use for when you need to step away for a minute

### Configuring Inputs and Sources
* Scroll all the way to the bottom, and find the "Customizable_Inputs" Scene
* Edit all the things to fit your stream
    * Edit "Text_Streamer_Name" to be your own name
    * Change the properties of "Main_Webcam" to point at your webcam
    * Edit the browser source for Browser_Latest_Donation and Browser_Top_Donation to change the "filterId" to match your extra life ID

## Getting External Data via Fragforce Servers

### Top/Last Donation for your Extra Life User
Getting the last or highest donation for your Extra Life team member account is simple using our server.  Just create a browser source with the following URL:
```
https://fragforce.org/static/ffsite/overlays/overlaytrack.html?listType=last&numDonations=1&filterId=401867
```
Change filterId to the Participant ID of your Extra Life user account.  **As of now, you MUST use individual participant IDS, not the Team ID**
You can change listType to 'top' to get the highest donation on your account as well!

To maintain consistent formatting, we recommend the following be placed in the CSS override portion of the browser source:
```
body { background-color: rgba(0, 0, 0, 0); margin: 0px auto; overflow: hidden; }
.textscroll { font-family: tricube; text-align: center; animation: none; font-size: 16px; color: #f09b00; }
```

## Theme Requirements
Transparent animated logos are being used in all scenes, and are encoded using VP8.  Issues can be most often resolved by updating your version of VLC, though please file an issue or reach out to us on our [Discord Server](http://discord.fragforce.org) if you have any problems.  Alternatively, you can use the static png logo included in this repository to reduce processing overhead and size.

## TODO List
- [ ] Fix Linux Instructions
- [ ] Change Individual Charity Logos to maybe animated rotating single logo?
- [ ] Create a super cool Theme Song to use

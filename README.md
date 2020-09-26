# FFOverlays
Graphics, Videos, and OBS configurations for Fragforce's Streams

## TL;DR - OBS Studio - Windows
* Install the 64 bit version of VLC from [HERE](https://www.videolan.org/vlc/download-windows.html) if you don't have it. 
* Download [the full repo zip](https://github.com/fragforce/FFOverlays/archive/master.zip)
* Extract the overlays folder to C:\Stream on Windows
* Install the fonts from the Fonts Folder onto your system
* Copy any EL/CMN videos you want to use for commercials in the C:\Stream\overlays\Commercials folder
* Import the Fragforce2020.json file into OBS (Scene Collection -> Import)
* Go change the specifics on in your configuration to point to your specific Extra Life account (see Configurable Content below)

## TL;DR - StreamLabs OBS - Temporarily deprecated, please use OBS official

## TL;DR - OBS Linux - Out of date, please nag at ParkerVCP to Fix this
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
The scene list is split into two different sections separated by a list of dashes in the scene list.  The first half is the group of usable visible scenes:

### FFOffline	
	Just the static offline image.  All streams
	should likely start here.

### IntroVideosOverlay
	This scene is a playlist of videos that can
	start the beginning of your stream, starting
	with a countdown timer, then the intro video
	and a few loops of the logo.  you will need to
	transition into your next scene manually during
	the logo loops to prevent stalling.

### IntroChatOneCam
	This scene shows your webcam along with some basic
	donation info and the twitch chat.  This can be your
	audience engagement screen, and is good to keep
	conversations logged in the VOD for future reference.

### 4:3GameLayout
	A gaming scene where the game you are playing is 
	traditional 'old school' TV aspect ratio, good
	for retro or some indie games.

### Game-43Cam-UpperInfoBar/Game-43Cam-LowerInfoBar
	These are your main gaming scenes, with the game
	taking the full stretch of the scene, and the
	only overlays being your webcam and the simple info bars.

### BRB-ELOverlay
	This is a simple static screen that will frame your Extra
	Life video ad rolls.  Good for breaks or transitions, or
	if you ever need to go take a break.  Cooler than ads, and
	better for the kids!


## Configurable Content
The bottom half of the scene list is the source for most of the streamable content above.  When you need to make changes to base items, youll be doing it down here.

### BotLayer
This is the basic overlay for the Fragforce Bot.  This should be left alone generally except for testing purposes.  You should add this scene to the very top of any and all new streamable scenes you create above.

### 4:3CamTitled/WSCamTitled
These are the raw sources for your framed webcams from above.
```
NamePlateMain - This should be changed to your stream handle
MainCam - This should be set to your webcam, or other scene
			where applicable
```
### Donation Panels
These four scenes (TopDonationPanel(Inv), LastDonationPanel(Inv)) are the dissassembled panels for your donation tracking.  
```
	TopDonoTitle/LastDonoTitle - the text plate for the associated
									info, change as needed
	BrowserTop(Last)Donation - these are browser sources to get the
								information from the server.  See
								formatting below for more info
```
### TopInfoBar/BottomInfoBar
The assembled pieces of the donation panels with a logo.  Use or modify as you see fit

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

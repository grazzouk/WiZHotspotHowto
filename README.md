# How-To: Set Up a Philips WiZ Smart Light to your Mobile Hotspot without a WiFi Router

The WiFi where I live was giving me a lot of trouble, and I live alone, so I chose not to even bother with it and just use my phone as a Mobile Internet Hotspot for all my internet needs. This was fine for most things, but setting up my WiZ Smart Lights turned out to be a bit of an issue, and needed some hacking to get working, so I figured I'd publish a little tutorial on how to get it done, mostly for myself but also for anyone else having this problem (or anyone who's just curious). I haven't tried it with anything other than Smart Lights on Android, so YMMV with other devices (although I'd be interested to hear the results if you tried this tutorial with anything else).

### Usage Notes
The lights will only be available when your hotspot is turned on and reachable by the lights, since they can't connect to anything if not. This also means that if you have a big house you might need to move into a specific room to be able to use a light, instead of having full coverage at all times, and you'll be unable to use your lights remotely if you're not home.

### Tutorial
First off: You'll need some kind of computer, since the app needs to _think_ it's connected to WiFi (but can actually successfully do everything through your mobile internet if you trick it to).

On your phone:
* Make sure you're connected to mobile internet
* Turn your WiFi Hotspot on 
	* For me this was under `Connections -> Mobile Hotspot and Tethering -> Mobile Hotspot`
* Note down the Phone's `Network name` and `Password` both for the next step (on your PC), and for entering later with the WiZ app.

On your computer: 
* Connect your computer to your WiFi hotspot using the `Network name` and `Password` in the settings.
* Start up a mobile hotspot on your computer by turning the `Off` switch in the `Mobile Hotspot` settings to `On`
	* You can find this under `Settings -> Network and Internet -> Mobile Hotspot`
	* Or just go to the start menu and type `Mobile Hotspot` and click the first option that comes up
* Turn power saving off so it doesn't disconnect mid way through this procedure
* Again, keep this page open for the Computer's Hotspot name and password

Back on the phone:
* Using the above credentials, connect to your Computer hotspot from the WiFi Settings of your phone (`Settings -> Connections -> WiFi`)
* Go to the Wiz App (download it from the play store if you don't have it already)
* Create a room if you need to (this doesn't require any sort of internet access)
* Press `Add a device`
* Click `Light`
* It'll autofill the SSID field with the Desktop Hotspot name, but this is **NOT** what you want. Luckily we can change it. Click on the `Enter SSID` field and type in your Phone's (not your desktops) Hotspot name, then enter the password for the Phone Hotspot
   * Note that while you should have it turned on for convienience, you should still be connected to your Desktop Hotspot at this stage. So your Phone Hotspot doesn't actually need to be broadcasting or connected to the internet just yet.
* Press `Continue`
* Wait for the tests to run (they'll take a while because of failure retries)
* You'll get an error message. For me the only the only thing that was ticked was "Broadcast on local network". This is fine. Just press the "Proceed Anyway" hyperlink at the bottom of the Network Diagnostics box
* Turn the WiFi off on your phone with the Quick Settings Dropdown
* Click `Start` under `Manual pairing`
* Follow the instructions on the next 2 screens (turn your light off then on 3 times until it's pulsing blue, then wait a moment for it to pulse purple), then press `Start` 
* Follow the instructions on this next page, connecting to the `WIZConfig_XXXX` WiFi
	* For me I needed to stay on the settings page until the "Internet may not be available" notification came up and click "Connect only this time" so that my phone would stay connected to the light
* Here's the tricky part (sadly right at the end): Wait for the "WiFi" popup to come up, let your phone connect to the WiFi for a second, then as soon as you see the WiFi is connected turn off the WiFi on your phone with the Quick Settings Dropdown
* Tada: It should say "All Done" and send you back to the main screen, where your Light will be fully set up and able to be controlled via the app

Remember to turn off your Mobile Hotspot on your computer (and to turn the Hotspot Power Saving option back on on there if you want that), and you're all set. Enjoy your smart lights, no WiFi router required!

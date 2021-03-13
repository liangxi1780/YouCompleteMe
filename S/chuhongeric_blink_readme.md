# Blink Shell for iOS
Do Blink! [Blink](http://u.720life.cn/g/5ab3518bc2b6310bce117d4ce19591ff)  is the first professional, desktop-grade terminal for iOS that leverages the support of Mosh and SSH. Thus, we can unequivocally guarantee stable connections, lightning-fast speeds, and full configurations. It can and should be your all-day-long tool.

We did not create another terminal to fix your website on the go. Blink was built as a professional grade product from the onset. We started by analyzing what the must-haves were and we ended up grounding Blink on these three concepts:
- Fast rendering: dmesg in your Unix server should be instantaneous. We can't wait even a second to render. We didn't need to reinvent the wheel to make this happen. We simply used Chromium's HTerm to ensure that rendering is perfect and fast, even with those special, tricky encodings.
- Always on: Mosh transcends SSH's variability. Mosh overcomes the unstable and intermittent connectivity that we all associate with mobile connections. You can check your Safari without fear of having to restart the SSH connection. You can flawlessly jump from home, to the train, and then the office thanks to Mosh. Blink is rock-solid connected all the way. Mosh is readily available and can be easily installed on your server. Go to https://mosh.org. 
- Fully configurable: Blink embraces Bluetooth-coupled keyboards with gusto. Some like Caps as Esc on Vim, others Caps as Ctrl on Emacs. Blink champions them all. But there's more, because we want more. You can also add your own custom themes and fonts to Blink. During your always-on sessions, you're in your zone.

But, Blink is much more. Please read on:
- You should command your terminal, not navigate it. Blink will jump you right into a friendly shell and it'll be clear to you how to roll.
- The interface is straightforward. We dumped all menus and went full screen for your terminal.
- Use swipe to move between your open connections, slide down to close them, and even pinch to zoom!
- Configure your Blink connections by adding your own Hosts and RSA Encryption keys. Everything will look familiar and you get to work, fast!
- We've incorporated SplitView, for those necessary Google searches and chats with coworkers.

For more information, please visit [Blink Shell](http://u.720life.cn/g/bc6e5174a284b6e6b3514c02f893039fc8603c8838ba5fe9d8cc22417eb495c2 

# Obtaining Blink
Blink is available now on the [AppStore](http://u.720life.cn/g/4625a951fe2763cda40b119796399bd5a02a0c5ef527f18666dd7fe04e345f9841c4a200d92045a3770676f2a0ad7417  Check it out!

If you would like to participate on its development, we would love to have you on board! There are two ways to collaborate with the project: you can download and build Blink yourself, or you can request an invitation to help us test future versions (on the raw branch). If you want to participate on the testing, follow and tweet us [@BlinkShell](http://u.720life.cn/g/5ea88169c4a0fbd169233d52478d54fe21f3c58a8157e068137b9f05e2af636b)  about your usage scenarios. Invitations will be sent out in waves, please be patient if you do not receive yours immediately.

Bugs should be reported here on GitHub. Crash reports will be automatically reported back to us thanks to HockeyApp. If you have any questions or want to make sure we do not miss on an interesting feature, please send your suggestions to our Twitter account [@BlinkShell](http://u.720life.cn/g/5ea88169c4a0fbd169233d52478d54fe8aa6e5bb1cfb5f6cad491797a31a79a8  We would love to discuss them with you! Please do not use Twitter to report bugs.

We can't wait to receive your valuable feedback. Enjoy!

## Build
We made a ton easier to build and install Blink yourself on your iOS devices through XCode. We provide a precompiled package with all the libraries for the master branch. Just extract this package in your Framework folder and build Blink.

```bash
git clone --recursive git@github.com:blinksh/blink.git && \
cd blink && ./get_frameworks.sh
```

Although this is the quickest method to get you up and running, if you would like to compile all libraries and resources yourself, refer to [BUILD](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ac459a3df4f7403cb8409527f0fb8c204ba5f59285a15605da44a978251c0979e90ebd49371e37e44b6bbe7c77456f43  Please let us know if you find any issues. Blink is a complex project with multiple low level dependencies and we are still looking for ways to simplify and automate the full compilation process.

# Using Blink
Our UI is very straightforward and optimizes the experience on touch devices for the really important part, the terminal. You will jump right into a very simple shell, so you will know what to do. Here are a few more tricks:
- Type 'help' to find information at the shell.
- Use two fingers tap to create a new shell.
- Move between shells by swapping your finger.
- You can exit the session and get back to the shell to open a new connection.
- You can also close a session by dragging two fingers down.
- Use pinch gesture to increase or reduce size of text. You can also use Cmd+ or Cmd- if using the keyboard.
- Copy and Paste by selecting text o tapping the screen.
- Run 'config' to setup your keys. Install them to a server through ssh-copy-id.
- Ctrl and Alt modifiers at the SmartKeys bar allow for continuous presses, like in a real keyboard.

# Changelog
# Version 10.0
	- Secured Mosh Persistent Connections and Restore.
	- Image rendering!
	- URL Links detection!
	- Autocomplete for commands and hosts!
	- Two fingers swipe up shows a new "control command" section.
	- Support for Remote Copy under SSH.
	- iPhone users, two fingers closes on-screen keyboard.
	- More and better emojis support.
	- Added "history" command to cleanup the history file.
	- Bold fonts now with an option for bold or bright.
	- New WWDC16 theme.
	- Added Light/Dark keyboard setting.
	- Support for installed fonts, so no more CSS is required.
	- Control selections with keyboard! Read help for more information.
	- Copy - Paste now works in unfocused mode too.
	- Paste Selection.

	- Faster Terminal rendering thanks to better writing flows.
	- Updated HTerm!
	- Updated Mosh to 1.3!
	- Updated MBProgressHUD to fix race conditions.

	- Fixed stuck Cmd key (deal with iOS issues).
	- Fixed swipe ups triggering SmartKeys.
	- Fixed Cmd as Ctrl for Ctrl+C and Ctlr+Z
	- Fixed resize glitches.
	- Improved loading time for terminal and custom fonts.
	- Improved focus when switching between apps.
	- Improved and smoother animations.
	- Improved accessoryView handling if other screen is active.
	- Improved all gestures internally.
	- Fixed tab caching after closed.
	- Fixed issues with irregular character widths misaligning columns.
	- Fixed vertical rendering of fonts in some specific scenarios.
	- Fixed issues with resizes and focus.
	- Fixed unselect on tap.
	- Fixed ssh restores crashing the app.
	- Fixed external screen focus.

[View all changes](CHANGELOG.md)

# Attributions
- [Mosh](http://u.720life.cn/g/949f8ae8fb0e037f4444779122b0eb8e)  was written by Keith Winstein, along with Anders Kaseorg, Quentin Smith, Richard Tibbetts, Keegan McAllister, and John Hood.
- This product includes software developed by the OpenSSL Project
for use in the OpenSSL Toolkit. (http://u.720life.cn/g/4f958e764157e985f98bcd747101b46dd676b0739bc7e5d2c07b7e7a05a47c17 
- [Libssh2](http://u.720life.cn/g/f0067ed230b7c6755994337ef711ed1cfc4eb97918c9446121d4342cd97338fe) 
- Entypo pictograms by Bruce Daniel www.entypo.com.



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)
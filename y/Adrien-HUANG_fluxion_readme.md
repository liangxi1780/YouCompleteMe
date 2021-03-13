![Fuxion logo](https://github.com/FluxionNetwork/fluxion/raw/master/logos/logo.jpg)

# Fluxion is the future of MITM WPA attacks
Fluxion is a security auditing and social-engineering research tool. It is a remake of linset by vk496 with (hopefully) fewer bugs and more functionality. The script attempts to retrieve the WPA/WPA2 key from a target access point by means of a social engineering (phishing) attack. It's compatible with the latest release of Kali (rolling). Fluxion's attacks' setup is mostly manual, but experimental auto-mode handles some of the attacks' setup parameters. Read the [FAQ](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467e36eeeee19e0f8ee578fec191b7c2ca331bff30a2e4e32e7d3ecc6d51803b08fddf5d98d8af2a5412fcec3d57ef45f0)  before requesting issues.

If you need quick help, fluxion is also available on gitter. You can talk with us on [Gitter](http://u.720life.cn/g/11e95d0ed8d2826912e12fe1dc3f3421573637e6fe285b1d38083b3036da5fb0fc5e8e9caa2caab318a30c00ea3a5f3a)  or on [Discord](http://u.720life.cn/g/f2a7d7b12e1fc16eaafd863db538a183918fba2ed3b9900726c47a3c24fe2a52 
## Installation
Read [here](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467e36eeeee19e0f8ee578fec191b7c2ca2a378c3576b9d267a519c066db22b36306ef9eeb21d29312079091627a7aa1f8)  before you do the following steps.
 
**Download the latest revision**
```
git clone git@github.com:FluxionNetwork/fluxion.git

# Or if you prefer https 

git clone https://www.github.com/FluxionNetwork/fluxion.git
```
**Switch to tool's directory**
```
cd fluxion 
```
**Run fluxion (missing dependencies will be auto-installed)**
```
./fluxion.sh
```

**Fluxion is also available in arch** 
```
cd bin/arch
makepkg
```

or using the blackarch repo
```
pacman -S fluxion
```

## :scroll: Changelog
Fluxion gets weekly updates with new features, improvements, and bugfixes.
Be sure to check out the [changelog here](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467e36eeeee19e0f8ee578fec191b7c2ca7b69aed39ea4118992bc72f675aaf960af927be931ca317edcdf2623f78462b8 

## :octocat: How to contribute
All contributions are welcome! Code, documentation, graphics, or even design suggestions are welcome; use GitHub to its fullest. Submit pull requests, contribute tutorials or other wiki content -- whatever you have to offer, it'll be appreciated but please follow the [style guide](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467e36eeeee19e0f8ee578fec191b7c2ca012e0cfc661149e51bef67ed57bed10a0081143080f651d585ccedd4da9cbcf19462496a889c06c07c701d00d8c364c3 

## :book: How it works
* Scan for a target wireless network.
* Launch the `Handshake Snooper` attack.
* Capture a handshake (necessary for password verification).
* Launch `Captive Portal` attack.
* Spawns a rogue (fake) AP, imitating the original access point.
* Spawns a DNS server, redirecting all requests to the attacker's host running the captive portal.
* Spawns a web server, serving the captive portal which prompts users for their WPA/WPA2 key.
* Spawns a jammer, deauthenticating all clients from original AP and luring them to the rogue AP.
* All authentication attempts at the captive portal are checked against the handshake file captured earlier.
* The attack will automatically terminate once a correct key has been submitted.
* The key will be logged and clients will be allowed to reconnect to the target access point.

* For a guide to the `Captive Portal` attack, read the [Captive Portal attack guide](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467e36eeeee19e0f8ee578fec191b7c2ca012e0cfc661149e51bef67ed57bed10a34dc5828238bb3022af0f585bd82c8b18b67253509be904b9585295b6f9cbbfe) 

## :heavy_exclamation_mark: Requirements

A Linux-based operating system. We recommend Kali Linux 2018.4. An external wifi card is recommended.

## Related work

For development, I use vim and tmux. Here are my [dotfiles](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046204d53f20fd09bf18df337e797ab84a227666e6c0a6af451b196cea2a1ccd31f) 
## :octocat: Credits
1. l3op - contributor
2. dlinkproto - contributor
3. vk496 - developer of linset
4. Derv82 - @Wifite/2
5. Princeofguilty - @webpages and @buteforce
6. Photos for wiki @http://www.kalitutorials.net
7. Ons Ali @wallpaper
8. PappleTec @sites
9. MPX4132 - Fluxion V3

## Disclaimer
* Authors do not own the logos under the `/attacks/Captive Portal/sites/` directory. Copyright Disclaimer Under Section 107 of the Copyright Act 1976, allowance is made for "fair use" for purposes such as criticism, comment, news reporting, teaching, scholarship, and research.

* The usage of Fluxion for attacking infrastructures without prior mutual consent could be considered an illegal activity and is highly discouraged by its authors/developers. It is the end user's responsibility to obey all applicable local, state and federal laws. Authors assume no liability and are not responsible for any misuse or damage caused by this program.

## Note
* Beware of sites pretending to be related with the Fluxion Project. These may be delivering malware.

* Fluxion **DOES NOT WORK** on Linux Subsystem For Windows 10, because the subsystem doesn't allow access to network interfaces. Any Issue regarding the same would be **Closed Immediately**

## Links
**Fluxion website:** https://fluxionnetwork.github.io/fluxion/  
**Discord:** https://discordapp.com/invite/G43gptk  
**Gitter:** https://gitter.im/FluxionNetwork/Lobby  



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)
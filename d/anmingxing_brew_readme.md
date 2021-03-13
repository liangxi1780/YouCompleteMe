# Homebrew
[![GitHub release](https://img.shields.io/github/release/Homebrew/brew.svg)](https://github.com/Homebrew/brew/releases)

Features, usage and installation instructions are [summarised on the homepage](http://u.720life.cn/g/0a2211bd9d9066fae8cdaf6612daaa9a30e266573a4962bb36b9bb795fbfabeb  Terminology (e.g. the difference between a Cellar, Tap, Cask and so forth) is [explained here](http://u.720life.cn/g/27ce355474c1b3938f5d9b5dc947ef04b10aa1f82ecc977e24230ff2d5fd58b4d54189d8aa19df2492025b999a1d11c302776e52ef80ce4e1a64265ad1a11446 

## What Packages Are Available?
1. Type `brew search` for a list.
2. Or visit [formulae.brew.sh](http://u.720life.cn/g/7c7c1a248d55b55e86779aadf8b9289a15f299ab4f9f719037e0fef184e5913f)  to browse packages online.
3. Or use `brew search --desc  ` to browse packages from the command line.

## More Documentation
`brew help`, `man brew` or check [our documentation](http://u.720life.cn/g/27ce355474c1b3938f5d9b5dc947ef0427debf1ef3d91446e533bcfa8b6d46a6 

## Troubleshooting
First, please run `brew update` and `brew doctor`.

Second, read the [Troubleshooting Checklist](http://u.720life.cn/g/27ce355474c1b3938f5d9b5dc947ef04d69660ed5b4201edcc2644b471088a43818ebd220bb18344e112faa6b149e419 

**If you don't read these it will take us far longer to help you with your problem.**

## Contributing
We'd love you to contribute to Homebrew. First, please read our [Contribution Guide](CONTRIBUTING.md) and [Code of Conduct](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f0dde756e73d3498c345aa2cdcac885bad73910847588d26b6a383310ca359309cdfb496ab7e32737c4f30f359a7e43f38921d3999c2839fcba992e392c485435698aa21643b17902969e018bfea2e16 

We explicitly welcome contributions from people who have never contributed to open-source before: we were all beginners once! We can help build on a partially working pull request with the aim of getting it merged. We are also actively seeking to diversify our contributors and especially welcome contributions from women from all backgrounds and people of colour.

A good starting point for contributing is running `brew audit --strict` with some of the packages you use (e.g. `brew audit --strict wget` if you use `wget`) and then read through the warnings, try to fix them until `brew audit --strict` shows no results and [submit a pull request](http://u.720life.cn/g/27ce355474c1b3938f5d9b5dc947ef047f51354f9d653f2a4665cc84b593caca790a5a13bd706b78da5b08c6a4dd2abbfcb1ac69cc5813da8b3240d2a29d7f9a  If no formulae you use have warnings you can run `brew audit --strict` without arguments to have it run on all packages and pick one.

Alternatively, for something more substantial, check out one of the issues labeled `help wanted` in [Homebrew/brew](http://u.720life.cn/g/54145d0471d91890860f7f8463c030469bb5ac076cd047a4dba58f33e69c10145d7119a4f117eb6236cafcdb26dc53463d8bf462be1dc163709c00504b2d3122639349d7de1c13fb53e628f03a0d22c6f871040a5a5bee32b44a88cf8131c74e)  or [Homebrew/homebrew-core](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463c332e8c891d3e3dd8fc74b4703037a76e0cb59ab8ead12fd29f82745921d199410b5b7191d574f33d104e47dd58c78d5c51b6af72b13d595913decf05020c9790628fe202a1d6356942f67017157d4d43731a254e3dae02f8f083f7c8c5da35 

Good luck!

## Donations
Homebrew is a non-profit project run entirely by unpaid volunteers. We need your funds to pay for software, hardware and hosting around continuous integration and future improvements to the project. Every donation will be spent on making Homebrew better for our users.

Please consider a regular donation through [GitHub Sponsors](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304607c0bc95d6daa96105f532eda045392425f52f9d5640661138694689e8e1418b)  or [Patreon](http://u.720life.cn/g/ebe7e576a80659072f312136d27e268129a41c89e9bcf9b6fea621b08995d26e8e429155b126494627caebe3b91fa6db 

Alternatively, if you'd rather make a one-off payment:

- [Donate with PayPal](http://u.720life.cn/g/a273b252b999cb4afe707ebbed9aa55c293f3951cd6fd11bf76cc8e3c67d86f913e3d58635fcad1d274fd24cd95d2c4d512bb492cbe1499d45e6af6502ef138811de7e0969da88eb8b65ab253be50bfc9556e471e073ce77a51d73d4da7588be) 
- Donate by USA $ check from a USA bank:
  - Make check payable to "Software Freedom Conservancy, Inc." and place "Directed donation: Homebrew" in the memo field. Checks should then be mailed to:
    - Software Freedom Conservancy, Inc.
      137 Montague ST  STE 380
      BROOKLYN, NY 11201             USA
- Donate by wire transfer: contact accounting@sfconservancy.org for wire transfer details.

Homebrew is a member of the [Software Freedom Conservancy](http://u.720life.cn/g/99f3cf71082f8ade4f1fc99866a8b98aee19d9d7f975741000c3717702e0a55d)  which provides us with an ability to receive tax-deductible, Homebrew earmarked donations (and [many other services](http://u.720life.cn/g/99f3cf71082f8ade4f1fc99866a8b98a39cf5010ff11d824d213c7cf3944bf17db10f4110cc6201083f8241d99bce0f6  Software Freedom Conservancy, Inc. is a 501(c)(3) organization incorporated in New York, and donations made to it are fully tax-deductible to the extent permitted by law.

## Security
Please report security issues to our [HackerOne](http://u.720life.cn/g/3cf0773f90ef5e9448fd98e79e9232212e60cc2af271878f73a23540deac47230364bd18cd1ae0a228f024c9ad6dcf83 

## Who Are You?
Homebrew's [Project Leader](http://u.720life.cn/g/27ce355474c1b3938f5d9b5dc947ef04ad3fbf7c153905c509063f30d468f8b235394e7a9f6252e554c363023c2a56c8b38c534f7b559c0ff3aaf6c6acad21d6)  is [Mike McQuaid](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460eaa59ac5113319ba3f4ee79bca1f918 

Homebrew's [Project Leadership Committee](http://u.720life.cn/g/27ce355474c1b3938f5d9b5dc947ef04ad3fbf7c153905c509063f30d468f8b2f1aa384882a2004aee57eb51c8c3c20c9a176802d947b024380272cad525fb5db2899bca705b0d250b03e6b97735d784)  is [Misty De Meo](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046383307d344aafd5f3e7b08d9aade3b02  [Shaun Jackman](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466e911c44fe635b9afb97bd7333b46484  [Jonathan Chang](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e8462196b6dbee4929bcd1f282d46354  [Sean Molenaar](http://u.720life.cn/g/54145d0471d91890860f7f8463c030468c83eae3684b20923c0adf8be92f62f3)  and [Markus Reiter](https://github.com/reitermarkus).

Homebrew's [Technical Steering Committee](http://u.720life.cn/g/27ce355474c1b3938f5d9b5dc947ef04ad3fbf7c153905c509063f30d468f8b23dcf3f4294305305418a7df6d80ff7737f0a5757fd1366e4234594107376166d14a7d2767a4fe6e6c70f7765bb352995)  is [Michka Popoff](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464a49e6e6fc73629d4ef500ac8a5b254b  [FX Coudert](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ff82a6cc51d8d6d0f66e973012f41e25  [Markus Reiter](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304629ed4f525124d81f4c28ecedd8a4b4d82b7f69ccecd5772062d33673caeab5b9  [Misty De Meo](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b473a0d8a62d269593850fcf45e0d245)  and [Mike McQuaid](https://github.com/MikeMcQuaid).

Homebrew/brew's Linux maintainers are [Michka Popoff](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464a49e6e6fc73629d4ef500ac8a5b254b  [Shaun Jackman](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466e911c44fe635b9afb97bd7333b46484  [Dawid Dziurla](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304606217838f703bf961a5356b4e9951577)  and [Issy Long](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b495e00d7a49996400214582d8a1dc05 

Homebrew's other current maintainers are [Claudia Pellegrino](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046482e8de03b3278d447b92975950924f4  [Zach Auten](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304634601faff71af00ebd8458ef96fb207b  [Rui Chen](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a68314f42045ea79cb6ff94cb5805781  [Vitor Galvao](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461d1bb8addf10701809a6f105993aea42  [Caleb Xu](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465ee7cb6aafd3da68615d28d2e31dfc7b  [Gautham Goli](https://github.com/GauthamGoli), [Steven Peters](https://github.com/scpeters), [Bo Anderson](https://github.com/Bo98), [William Woodruff](https://github.com/woodruffw), [Igor Kapkov](https://github.com/igas), [Sam Ford](https://github.com/samford), [Alexander Bayandin](https://github.com/bayandin), [Izaak Beekman](https://github.com/zbeekman), [Eric Knibbe](https://github.com/EricFromCanada), [Viktor Szakats](https://github.com/vszakats), [Thierry Moisan](https://github.com/moisan), [Steven Peters](https://github.com/scpeters), [Tom Schoonjans](https://github.com/tschoonj) and [Issy Long](https://github.com/issyl0).

Former maintainers with significant contributions include [Jan Viljanen](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046847944c93b2f621410bde914f1197dd6  [JCount](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d702d31b232d9b6e66452141c1b13f1b  [commitay](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046501e4d29b220d277de0b8dd2be40190b  [Dominyk Tiller](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304644812cef22b4f738229dab518797cfd0  [Tim Smith](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304646ac807b3668f07ec3886ea056b3c07b  [Baptiste Fontaine](https://github.com/bfontaine), [Xu Cheng](https://github.com/xu-cheng), [Martin Afanasjew](https://github.com/UniqMartin), [Brett Koonce](https://github.com/asparagui), [Charlie Sharpsteen](https://github.com/Sharpie), [Jack Nagel](https://github.com/jacknagel), [Adam Vandenberg](https://github.com/adamv), [Andrew Janke](https://github.com/apjanke), [Alex Dunn](https://github.com/dunn), [neutric](https://github.com/neutric), [Tomasz Pajor](https://github.com/nijikon), [Uladzislau Shablinski](https://github.com/vladshablinsky), [Alyssa Ross](https://github.com/alyssais), [ilovezfs](https://github.com/ilovezfs), [Chongyu Zhu](https://github.com/lembacon) and Homebrew's creator: [Max Howell](https://github.com/mxcl).

## Community
- [discourse.brew.sh (forum)](http://u.720life.cn/g/60634847e115fbca3ab3ef25b33bebff5d71998c6a73ca18122372eac61e4e1a) 
- [freenode.net\#machomebrew (IRC)](irc://irc.freenode.net/#machomebrew)
- [@MacHomebrew (Twitter)](http://u.720life.cn/g/5ea88169c4a0fbd169233d52478d54fe58f7ac3434002468a63357b81c8f7e43) 

## License
Code is under the [BSD 2-clause "Simplified" License](LICENSE.txt).
Documentation is under the [Creative Commons Attribution license](http://u.720life.cn/g/f92437de2a0f19dbeda7f9325abcfd61608973388e99646292f37c07cffde07915d5c9dce57380173dfca662967230cb 

## Sponsors
Our macOS continuous integration infrastructure is hosted by [MacStadium's Orka](http://u.720life.cn/g/1da3b8ea072c152a5ac66458312c87f4b2453b26e96da730165106c5e9d43faac78718e744687c89b6eb2aa0edd4cf7d 

[![Powered by MacStadium](https://cloud.githubusercontent.com/assets/125011/22776032/097557ac-eea6-11e6-8ba8-eff22dfd58f1.png)](https://www.macstadium.com)


Our bottles (binary packages) are hosted by [Bintray](http://u.720life.cn/g/30aa4dd72d94f39a9fd13b96c7f343668b9826302926ade64f1d1325ed79195e 

[![Downloads by Bintray](https://bintray.com/docs/images/downloads_by_bintray_96.png)](https://bintray.com/homebrew)

Secure password storage and syncing is provided by [1Password for Teams](http://u.720life.cn/g/2936b8c4fc63ff7a1d8f5dcd49df65111463b14f0dc1751a9b96bc216643d8bf)  by [AgileBits](http://u.720life.cn/g/fc8bf42d63701f052712f0abccc864feb2f85d0a703703a652b0ed6681cc68c4 

[![AgileBits](https://da36klfizjv29.cloudfront.net/assets/branding/agilebits-fcca96e9b8e815c5c48c6b3e98156cb5.png)](https://agilebits.com)

Homebrew is a member of the [Software Freedom Conservancy](http://u.720life.cn/g/99f3cf71082f8ade4f1fc99866a8b98ad2e41e4e676923549565f8aea0f061ac 

[![Software Freedom Conservancy](https://sfconservancy.org/img/conservancy_64x64.png)](https://sfconservancy.org)



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)
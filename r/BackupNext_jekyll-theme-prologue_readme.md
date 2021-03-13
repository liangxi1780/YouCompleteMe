# Prologue - Jekyll Theme

[![Gem Version](https://badge.fury.io/rb/jekyll-theme-prologue.svg)](https://badge.fury.io/rb/jekyll-theme-prologue)

![Prologue Theme](assets/images/screenshot.png "Prologue Theme Screenshot")

This is Prologue, a simple, single page responsive site template from [HTML5 UP](http://u.720life.cn/g/47817f13f0b72265177b35d2f6ac03ff386b8015a9183bcf92a2aed9039de11f  now available as a blog-aware Jekyll theme from [Chris Bobbe](http://u.720life.cn/g/bc5f186cfdd14a33db36af4f8f2c38d383493d6532bacbfbabb32f9a1275a79e  It features a clean, minimalistic design and a sticky sidebar with navigation-linked scrolling.

**Demo**: https://chrisbobbe.github.io/jekyll-theme-prologue/

# Added Features

* **Blogging and multi-page features you expect from Jekyll**
* Compatible with GitHub Pages
* **[Formspree.io](http://u.720life.cn/g/f3a90a0218632f1c8d0aa9f2477715fdf8eac3de306e27df3b71bbb338d82ef7)  contact form integration** - just add your email to the `_config.yml` and it works!
* Build your homepage with **custom scrolly sections** in the _sections folder
 * Set a **cover photo** for any section (not just the first), with alt text for screen readers and SEO
* Add your **social profiles** easily in `_config.yml`.
* Automatic search engine optimization (SEO) **meta tags** based on info you provide in `_config.yml` and frontmatter
* **Google Analytics** built-in; just put your [Tracking ID](http://u.720life.cn/g/3f6bc38e6938b6711866a3ba7ee64d801de335b4ddc994dbe1cb2c292ea3021a89a8b6e801f23d0c9025ded383336134f1720cdb000aaba926a412cf022db112)  in `_config.yml` as `google_analytics`
* Custom **404 page** (called 404.html; to activate, move it to your project directory).

# Installation

There are two ways to get started (choose one):

1. **Install the [jekyll-theme-prologue gem](http://u.720life.cn/g/577cd196a5aaff883a4cee7f135a25fdc001cac5dc1408328f73076ae9666b00cf9f9cc0437ca5f94d111c7c14ee953cca8ca9fe763c30c45cda803eb2d07c0e  Instructions are in the [Jekyll docs](http://u.720life.cn/g/6a21ed45e167b1aa1cd0b5f81e69eba96d5756316275221c2e5dc524796cd18750cac1143c39952db562f7b3108697feeac4c0cd876c18cd3f6d404148636f08  After running `bundle install`, you can find the theme files by running `open $(bundle show jekyll-theme-prologue)`.  A sample working `_config.yml` file ships with the gem; if you want to activate it, move it to your project's root directory. It will do nothing until you move it there, replacing the default `_config.yml` file.
2. **Fork or clone the [GitHub repository](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304602021945254cd3722ee5a2566b85f601051dc50a6663797e080c13875dae34d5e79db97d57b38ad9ac63c92c28d78f5d  If you want to use [GitHub Pages](http://u.720life.cn/g/e74b692a81996e1b2ed64adb89491db269c871808dfb1e7a5c141a62e5a3dd45  create a branch named `gh-pages`, and replace `theme: jekyll-theme-prologue` with `remote_theme: chrisbobbe/jekyll-theme-prologue` in the provided `_config.yml` ([GitHub Pages now supports open-source themes on GitHub](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460a5c28efeb6881f934482d541286b078c41aec9e7c437da919f8d0de121c51718fa3bd3adafa12d82662e78e2ece0329 

Next, make sure that `url` and `base_url` are set for your own website in `_config.yml`. For local testing, make them both blank. Add a photo avatar to your project, then set `avatar: path/to/your/avatar.jpg` in _config.yml; for example, `avatar: assets/images/avatar.jpg` (48x48 pixels works best). Poke around the sample `_config.yml` file to see how you can add your social profiles.

# Build your homepage

1. **Your `_config.yml` file must include the following line or your homepage won't work**: `collections: [sections]`. This tells Jekyll to look in the _sections folder (which you will create) for your content and render it all on one page.

2. **Create a `_sections` folder** in your project's root directory and start adding content to your homepage. Set a cover photo in any of the sections by adding `cover-photo: path/to/photo.jpg` and `cover-photo-alt: your alt text here` to the section's frontmatter. Sample content is provided in the [GitHub repository](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304602021945254cd3722ee5a2566b85f601051dc50a6663797e080c13875dae34d55def5ec79138178be03a20d4f15b0356644bb2c848ddc60e2914fe037ffc26b5 

All new sections should be added as html or Markdown documents in the `_sections` folder. The following section variables can be set with [frontmatter](http://u.720life.cn/g/6a21ed45e167b1aa1cd0b5f81e69eba9d6e8d9c9bf18eb395a386a1c05d295b699265fbbc7f08fddee6e21062515f546 
- `title` (required)
- `order` (required; orders the sequence of sections on the page. Example: `1`)
- `cover-photo` (optional; sets a background image for the section. Example: `assets/images/banner.jpg`)
- `cover-photo-alt` (required if using a cover photo. Describes the photo for screen readers and SEO; e.g. "Dome of Light art installation, Kaohsiung, Taiwan")
- `icon` (optional; see [Font Awesome](http://u.720life.cn/g/d2f77437f3677ed437cd304d49efe896451a2eba61377d7650f6b59247cdeb89)  for icon codes. Example: `fa-github`)
- `icon-style` (optional; "solid" is default, "regular" for outline style icons, or "brands" for logos)
- `auto-header` (optional; "use-title" is default, "none" for no header, or custom header text)
- `hide` (optional; if `true`, the section won't appear)

# Start blogging!

Jekyll has great resources to get you started writing blog posts. Check out [this Jekyll Docs page](http://u.720life.cn/g/6a21ed45e167b1aa1cd0b5f81e69eba91c5072c3353f5a9f4c2f18dfd6683f72)  first. When you've written a post or two, copy the following into a new file in your project directory called `blog.html`, and you'll see a link to your blog from the homepage:

```
---
layout: blog
title: My Blog
---
```

-- and that's it!

# Add a page

To add a page, just make a new .html or .md file in your project directory. There's an example called `reading-list` [provided](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304602021945254cd3722ee5a2566b85f601051dc50a6663797e080c13875dae34d56ec49c7020bf4fac779df1e4abfbb73ef273da3b7572e2648ab29cd182b3b7a0)  with the GitHub repository. Add this frontmatter:

```
---
title: My New Page
layout: page
---
```

You can also set these page variables in the frontmatter, if you want:
- `subtitle`
- `order` (orders links in the nav menu, e.g. `1`)
- `icon` (optional; see [Font Awesome](http://u.720life.cn/g/d2f77437f3677ed437cd304d49efe896451a2eba61377d7650f6b59247cdeb89)  for icon codes. Example: `fa-github`)
- `icon-style` (optional; "solid" is default, "regular" for outline style icons, or "brands" for logos)
- `hide` (optional; if `true`, a link won't appear in the nav menu. All this does is remove the nav link; your page will still be served to anyone who has the URL.)

**This same set of frontmatter variables (including `title`) can also be set in `index.md` and `blog.html`.** You may want to give them titles, or hide the homepage link with `hide: true` if the homepage is the only page.

For advanced SEO, this theme also lets you add `permalink` (see [Jekyll Docs](http://u.720life.cn/g/6a21ed45e167b1aa1cd0b5f81e69eba958a2b85a109e431a039e902f4f6d331ef845fa68247ed7822f4c8144fa5de0898fb247a12ee841cf8d505154433443f941c9521c587022f8962ff4cfbe737c32  `robots` (string, e.g. "noindex, nofollow"), and `canonical` (boolean; true is default) to any page or post.

# Contributing

Please feel free to submit issues and feature requests!

# Credits

Thanks to @andrewbanchich for his many Jekyll adaptations of HTML5 UP's elegant themes, which helped and inspired me, and of course many thanks to HTML5 UP.

Original README from HTML5 UP:

```
Prologue by HTML5 UP
html5up.net | @ajlkn
Free for personal and commercial use under the CCA 3.0 license (html5up.net/license)


This is Prologue, a simple, single page responsive site template. It features a
clean, minimalistic design and a sticky sidebar with navigation-linked scrolling.

Demo content images* are courtesy of the ridiculously talented Felicia Simion. Check out
more of her amazing work over at deviantART:

http://ineedchemicalx.deviantart.com/

(* = Not included! Only meant for use with my own on-site demo, so please do NOT download
and/or use any of Felicia's work without her explicit permission!)

Demo banner images* courtesy of Unsplash, a radtastic collection of CC0 (public domain)
images you can use for pretty much whatever.

(* = Not included)

AJ
aj@lkn.io | @ajlkn

PS: Not sure how to get that contact form working? Give formspree.io a try (it's awesome).


Credits:

	Demo Images:
		Felicia Simion (ineedchemicalx.deviantart.com)
		Unsplash (unsplash.com)

	Icons:
		Font Awesome (fortawesome.github.com/Font-Awesome)

	Other
		jQuery (jquery.com)
		html5shiv.js (@afarkas @jdalton @jon_neal @rem)
		CSS3 Pie (css3pie.com)
		background-size polyfill (github.com/louisremi)
		Respond.js (j.mp/respondjs)
		jquery.scrolly (@ajlkn)
		jquery.scrollzer (@ajlkn)
		Skel (skel.io)
```



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)
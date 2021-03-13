# [Basically Basic Jekyll Theme][1]

[![LICENSE](https://img.shields.io/badge/license-MIT-lightgrey.svg)](https://github.com/mmistakes/jekyll-theme-basically-basic/blob/master/LICENSE)
[![Jekyll](https://img.shields.io/badge/jekyll-%3E%3D%203.6-blue.svg)](https://jekyllrb.com/)
[![Ruby gem](https://img.shields.io/gem/v/jekyll-theme-basically-basic.svg)](https://rubygems.org/gems/jekyll-theme-basically-basic)
[![Tip Me via PayPal](https://img.shields.io/badge/PayPal-tip%20me-green.svg?logo=paypal)](https://www.paypal.me/mmistakes)

Basically Basic is a [Jekyll theme](http://u.720life.cn/g/6a21ed45e167b1aa1cd0b5f81e69eba96d5756316275221c2e5dc524796cd18714480b14a0beee6a37a9c644e71c814a)  meant as 
a substitute for the default [Minima](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c118f2b5609c9865ea6387ad7d5e91706c741135e6aadd23f4d6e261ff4e5e6c  with a 
few enhancements thrown in for good measure:

- Clean responsive design with [six customizable skins](#skin)
- Curriculum Vitæ/Resume layout powered by [JSON data](http://u.720life.cn/g/ab2bf93b726c7cfc95725d15781f717ca3baff1c8eea16e4f02fb591b8d77160) 
- About page layout
- Site-wide search provided by [Algolia](http://u.720life.cn/g/de5ac60d0586b8305e0a1e36246bd201758b9e777a122767a56de150af356c7c)  or [Lunr](http://u.720life.cn/g/0ff7795f9f48ff91ce512612eeef5cc12bbb86b09faafdf6b139b71dcddd1025 
- Disqus Comments and Google Analytics support
- SEO best practices via [Jekyll SEO Tag](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304654dd3c9dbefe48a50b90ea6ba5c85f2edfd025bd865a7be50eb6ae11d3b27179) 

**If you enjoy this theme, please consider [supporting me](http://u.720life.cn/g/a273b252b999cb4afe707ebbed9aa55cd9e3dd07dd000a23c5c5d4e91667c44c)  for developing and maintaining it.**

[![Support via PayPal](https://cdn.rawgit.com/twolfson/paypal-github-button/1.0.0/dist/button.svg)](https://www.paypal.me/mmistakes)

[![Basically Basic live preview][2]][1]

[1]: https://mmistakes.github.io/jekyll-theme-basically-basic/
[2]: https://cloud.githubusercontent.com/assets/1376749/24117647/6dede894-0d81-11e7-9c2c-f19bea45e219.jpg (live preview)

## Table of Contents

1. [Installation](#installation)
   1. [Ruby Gem Method](#ruby-gem-method)
   2. [GitHub Pages Method](#github-pages-method)
      1. [Remove the Unnecessary](#remove-the-unnecessary)
2. [Upgrading](#upgrading)
   1. [Ruby Gem](#ruby-gem)
   2. [Remote Theme](#remote-theme)
   3. [Use Git](#use-git)
      1. [Pull Down Updates](#pull-down-updates)
   4. [Update Files Manually](#update-files-manually)
3. [Structure](#structure)
   1. [Starting Fresh](#starting-fresh)
   2. [Starting from `jekyll new`](#starting-from-jekyll-new)
4. [Configuration](#configuration)
   1. [Skin](#skin)
   2. [Google Fonts](#google-fonts)
   3. [Text](#text)
   4. [Navigation](#navigation)
   5. [Pagination](#pagination)
   6. [Search](#search)
      1. [Lunr (default)](#lunr-default)
      2. [Algolia](#algolia)
   7. [Author](#author)
   8. [Reading Time](#reading-time)
   9. [Comments (via Disqus)](#comments-via-disqus)
   10. [Google Analytics](#google-analytics)
   11. [Copyright](#copyright)
5. [Layouts](#layouts)
   1. [`layout: default`](#layout-default)
   2. [`layout: post`](#layout-post)
   3. [`layout: page`](#layout-page)
   4. [`layout: home`](#layout-home)
   5. [`layout: posts`](#layout-posts)
   6. [`layout: categories`](#layout-categories)
   7. [`layout: tags`](#layout-tags)
   8. [`layout: collection`](#layout-collection)
   9. [`layout: category`](#layout-category)
   10. [`layout: tag`](#layout-tag)
   11. [`layout: about`](#layout-about)
   12. [`layout: cv`](#layout-cv)
6. [Images](#images)
7. [Customization](#customization)
   1. [Overriding Includes and Layouts](#overriding-includes-and-layouts)
   2. [Customizing Sass (SCSS)](#customizing-sass-scss)
   3. [Customizing JavaScript](#customizing-javascript)
   4. [SVG Icons](#svg-icons)
   5. [Customizing Sidebar Content](#customizing-sidebar-content)
8. [Development](#development)
9. [Contributing](#contributing)
10. [Credits](#credits)
11. [License](#license)

## Installation

If you're running Jekyll v3.5+ and self-hosting you can quickly install the 
theme as a Ruby gem. If you're hosting with GitHub Pages you can install as a 
remote theme or directly copy all of the theme files (see [structure](#structure) 
below) into your project.

### Ruby Gem Method

1. Add this line to your Jekyll site's `Gemfile`:

   ```ruby
   gem "jekyll-theme-basically-basic"
   ```
2. Add this line to your Jekyll site's `_config.yml` file:

   ```yaml
   theme: jekyll-theme-basically-basic
   ```

2. Then run [Bundler](http://u.720life.cn/g/be29227eb4502832cc5f9bbd2330fc66258e456e10021710004d15d200b7f00b)  to install the theme gem and dependencies:
   
   ```terminal
   bundle install
   ```

### GitHub Pages Method

GitHub Pages has added [full support](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460a5c28efeb6881f934482d541286b078c41aec9e7c437da919f8d0de121c51716d55daccf01518a477e2aa2003502f01)  
for any GitHub-hosted theme.

1. Replace `gem "jekyll"` with:

   ```ruby
   gem "github-pages", group: :jekyll_plugins
   ```

2. Run `bundle update` and verify that all gems install properly.

3. Add `remote_theme: "mmistakes/jekyll-theme-basically-basic"` to your 
   `_config.yml` file. Remove any other `theme:` or `remote_theme:` entries.

---

**Note:** Your Jekyll site should be viewable immediately at 
 . If it's not, you can force a rebuild by 
**Customizing Your Site** (see below for more details).

If you're hosting several Jekyll based sites under the same GitHub username you 
will have to use Project Pages instead of User Pages. Essentially you rename the 
repo to something other than **USERNAME.github.io** and create a `gh-pages` 
branch off of `master`. For more details on how to set things up check 
[GitHub's documentation](http://u.720life.cn/g/1f425b0b33da40ebdfbaffd56fc94509ec09346c8015e0ae429751be8b3a78a5ff758ccd1bc20fa55ead2b9ac64b7dc26820f081359c1eb4aef085cc809afc531bb7a46f0bd9eb7ea8fd866a40f08fa6 

#### Remove the Unnecessary

If you forked or downloaded the `jekyll-theme-basically-basic` repo you can 
safely remove the following files and folders:

- `.editorconfig`
- `.gitattributes`
- `.github`
- `.scss-lint.yml`
- `CHANGELOG.md`
- `jekyll-theme-basically-basic.gemspec`
- `LICENSE`
- `Rakefile`
- `README.md`
- `screenshot.png`
- `/docs`
- `/example`

## Upgrading

If you're using the Ruby Gem or remote theme versions of Basically Basic, 
upgrading is fairly painless.

To check which version you are currently using, view the source of your built 
site and you should something similar to:

```
 
```

At the top of every `.html` file, `/assets/css/main.css`, and `/assets/js/main.js`.

### Ruby Gem

Simply run `bundle update` if you're using Bundler (have a `Gemfile`) or `gem 
update jekyll-theme-basically-basic` if you're not.

### Remote Theme

When hosting with GitHub Pages you'll need to push up a commit to force a 
rebuild with the latest [theme release](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467fa3a48c5c264ad05526b8732aee7dbc50fb2c65d9d24e4014e7524f30b65600f8e8305559a09d8d233280a4f0f412b3f11c5abae491a560f7e930c65f6c7be9 

An empty commit will get the job done too if you don't have anything to push at 
the moment:

```terminal
git commit --allow-empty -m "Force rebuild of site"
```

### Use Git

If you want to get the most out of the Jekyll + GitHub Pages workflow, then 
you'll need to utilize Git. To pull down theme updates you must first ensure 
there's an upstream remote. If you forked the theme's repo then you're likely 
good to go.

To double check, run `git remote -v` and verify that you can fetch from `origin https://github.com/mmistakes/jekyll-theme-basically-basic.git`.

To add it you can do the following:

```terminal
git remote add upstream https://github.com/mmistakes/jekyll-theme-basically-basic.git
```

#### Pull Down Updates

Now you can pull any commits made to theme's `master` branch with:

```terminal
git pull upstream master
```

Depending on the amount of customizations you've made after forking, there's 
likely to be merge conflicts. Work through any conflicting files Git flags, 
staging the changes you wish to keep, and then commit them.

### Update Files Manually

Another way of dealing with updates is [downloading the theme](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467fa3a48c5c264ad05526b8732aee7dbc50fb2c65d9d24e4014e7524f30b65600a5ab60e9ade8b6b1685be83da67d5021f1162e9b0a763c5fbc1414f1dfba4809)  
--- replacing your layouts, includes, and assets with the newer ones manually. 
To be sure that you don't miss any changes it's probably a good idea to review 
the theme's [commit history](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467fa3a48c5c264ad05526b8732aee7dbc50fb2c65d9d24e4014e7524f30b65600551afed2c63e6fe5c395f1d5c1eca6b97bb3584c38d63a36f71c07f1a6a0f8b2)  
to see what's changed since.

Here's a quick checklist of the important folders/files you'll want to be 
mindful of:

| Name                   |     |
| ----                   | --- |
| `_layouts`             | Replace all. Apply edits if you customized any layouts. |
| `_includes`            | Replace all. Apply edits if you customized any includes. |
| `assets`               | Replace all. Apply edits if you customized stylesheets or scripts. |
| `_sass`                | Replace all. Apply edits if you customized Sass partials. |
| `_data/theme.yml`      | Safe to keep. Verify that there were no major structural changes or additions. |
| `_config.yml`          | Safe to keep. Verify that there were no major structural changes or additions. |

---

**Note:** If you're not seeing the latest version, be sure to flush browser and 
CDN caches. Depending on your hosting environment older versions of 
`/assets/css/main.css`, `/assets/js/main.js`, or `*.html` may be cached.

## Structure

Layouts, includes, Sass partials, and data files are all placed in their default 
locations. Stylesheets and scripts in `assets`, and a few development related 
files in the project's root directory.

**Please note:** If you installed Basically Basic via the Ruby Gem method, theme 
files found in `/_layouts`, `/_includes`, `/_sass`, and `/assets` will be 
missing. This is normal as they are bundled with the [`jekyll-theme-basically-basic`](http://u.720life.cn/g/577cd196a5aaff883a4cee7f135a25fdc001cac5dc1408328f73076ae9666b004bb68a7eab6c57f6a0ae8d524ecba6a1bc98f78d30eb165d8d1980f0f2d66108)  gem.

```terminal
jekyll-theme-basically-basic
├── _data                      # data files
|  └── theme.yml               # theme settings and custom text
├── _includes                  # theme includes and SVG icons
├── _layouts                   # theme layouts (see below for details)
├── _sass                      # Sass partials
├── assets
|  ├── javascripts
|  |  └── main.js
|  └── stylesheets
|     └── main.scss
├── _config.yml                # sample configuration
└── index.md                   # sample home page (all posts/not paginated)
```

### Starting Fresh

After creating a `Gemfile` and installing the theme you'll need to add and edit 
the following files:

- [`_config.yml`](_config.yml)
- [`/_data/theme.yml`](_data/theme.yml)
- [`index.md`](index.md) 

**Note:** Consult the [**pagination**](#pagination) documentation below for
instructions on how to enable it for the home page.

### Starting from `jekyll new`

Using the `jekyll new` command will get you up and running the quickest.

Edit `_config.yml` and create `_data/theme.yml` as instructed above and you're 
good to go.

## Configuration

Configuration of site-wide elements (`lang`, `title`, `description`, `logo`, 
`author`, etc.) happens in your project's `_config.yml`. See the 
[example configuration](example/_config.yml) in this repo for additional 
reference.

|                    | Description                                                               |
| ------------------ | ------------------------------------------------------------------------- |
| `lang`             | Used to indicate the language of text (e.g., en-US, en-GB, fr)            |
| `title`            | Your site's title (e.g., Dungan's Awesome Site)                           |
| `description`      | Short site description (e.g., A blog about grasshopper mash)              |
| `url`              | The full URL to your site (e.g., https://groverloaf.org)                  |
| `author`           | Global author information (see below)                                     |
| `logo`             | Path to a site-wide logo ~100x100px (e.g., /assets/your-company-logo.png) |
| `twitter_username` | Site-wide Twitter username, used as a link in sidebar                     |
| `github_username`  | Site-wide GitHub username, used as a link in sidebar                      |

For more configuration options be sure to consult the documentation for: 
[**jekyll-seo-tag**][jekyll-seo-tag], [**jekyll-feed**][jekyll-feed], 
[**jekyll-paginate**][jekyll-paginate], and [**jekyll-sitemap**][jekyll-sitemap].

[jekyll-seo-tag]: https://github.com/jekyll/jekyll-seo-tag
[jekyll-feed]: https://github.com/jekyll/jekyll-feed
[jekyll-paginate]: https://github.com/jekyll/jekyll-paginate
[jekyll-sitemap]: https://github.com/jekyll/jekyll-sitemap

### Skin

This theme comes in six different skins (color variations). To change skins add 
one of the following to your [`/_data/theme.yml`](_data/theme.yml) file:

| `skin: default` | `skin: night` | `skin: plum` |
| --- | --- | --- |
| ![default-skin](https://cloud.githubusercontent.com/assets/1376749/24115744/c0618c90-0d7a-11e7-8e2d-ec70f9db0c1b.png) | ![night-skin](https://cloud.githubusercontent.com/assets/1376749/24115770/d61127f8-0d7a-11e7-9158-986bee2be8e7.png) | ![plum-skin](https://cloud.githubusercontent.com/assets/1376749/24115778/db523a0e-0d7a-11e7-9452-8692b736d67e.png) |

| `skin: sea` | `skin: soft` | `skin: steel` |
| --- | --- | --- |
| ![sea-skin](https://cloud.githubusercontent.com/assets/1376749/24115788/e27d818a-0d7a-11e7-8c56-2480e9ae83fb.png) | ![soft-skin](https://cloud.githubusercontent.com/assets/1376749/24115790/e6e548e8-0d7a-11e7-8e2d-d8053e8befd1.png) | ![steel-skin](https://cloud.githubusercontent.com/assets/1376749/24115799/eb2108e8-0d7a-11e7-8cc3-a6f22e4082ee.png) |

### Google Fonts

This theme allows you to easily use [Google Fonts](http://u.720life.cn/g/215b706e92c30f831f42c75448c4994be1180ba667851de590295c7a06052d23)  
throughout the theme. Simply add the following to your 
[`/_data/theme.yml`](_data/theme.yml), replacing the font `name` and `weights` 
accordingly.

```yaml
google_fonts:
  - name: "Fira Sans"
    weights: "400,400i,600,600i"
  - name: "Fira Sans Condensed"
```

### Text

To change text found throughout the theme add the following to your 
[`/_data/theme.yml`](_data/theme.yml) file and customize as necessary.

```yaml
t:
  skip_links: "Skip links"
  skip_primary_nav: "Skip to primary navigation"
  skip_content: "Skip to content"
  skip_footer: "Skip to footer"
  menu: "Menu"
  search: "Search"
  site_search: "Site Search"
  results_found: "Result(s) found"
  search_placeholder_text: "Enter your search term..."
  home: "Home"
  newer: "Newer"
  older: "Older"
  email: "Email"
  subscribe: "Subscribe"
  read_more: "Read More"
  posts: "Posts"
  page: "Page"
  of: "of"
  min_read: "min read"
  present: "Present"
```

### Navigation

By default all internal pages with a `title` will be added to the "off-canvas" 
menu. For more granular control and sorting of these menu links:

1. Create a custom list to override the default setting by adding a 
`navigation_pages` array to your [`/_data/theme.yml`](_data/theme.yml) file. 

2. Add raw page paths in the order you'd like:

   ```yaml
   navigation_pages:
     - about.md
     - cv.md
   ```

Each menu link's title and URL will be populated based on their `title` and 
`permalink` respectively.

### Pagination

Break up the main listing of posts into smaller lists and display them over 
multiple pages by [enabling pagination](http://u.720life.cn/g/41b49956459f45e009beb54ff3039b859a60e25e4718a168f4019de1d03cd6c8cd01c40d9df13d6ab8f469bab7eaf475 

1. Include the `jekyll-paginate` plugin in your `Gemfile`.

   ```ruby
   group :jekyll_plugins do
     gem "jekyll-paginate"
   end
   ```

2. Add `jekyll-paginate` to `gems` array in your `_config.yml` file and the 
following pagination settings:

   ```yaml
   paginate: 5  # amount of posts to show per page
   paginate_path: /page:num/
   ```

3. Create `index.html` (or rename `index.md`) in the root of your project and 
add the following front matter:

   ```yaml
   layout: home
   paginate: true
   ```

### Search

To enable site-wide search add `search: true` to your `_config.yml`.

#### Lunr (default)

The default search uses [**Lunr**](http://u.720life.cn/g/0ff7795f9f48ff91ce512612eeef5cc1c674a2483b10b7338fe5e1ccd1c783ed)  to build a search index of all your documents. This method is 100% compatible with sites hosted on GitHub Pages.

**Note:** Only the first 50 words of a post or page's body content is added to the Lunr search index. Setting `search_full_content` to `true` in your `_config.yml` will override this and could impact page load performance.

#### Algolia

For faster and more relevant search ([see demo](http://u.720life.cn/g/ec025fd50ec7b372ca55857247a3257d2ffcb3a50df450f20488e4645713022dc03c3730dcb7d61762d2b31da4fc1efbee74b0ec6329b95c5f158f2db9c6c2cecc77e22fa138e505e34cc8eb1ad98535 

1. Add the [`jekyll-algolia`](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046661b7a621afe563822afc2bf34a375fb3e6d10a3a9d7ebbc660ab738bb0c709a)  gem to your `Gemfile`, in the `:jekyll_plugins` section.

   ```ruby
   group :jekyll_plugins do
     gem "jekyll-feed"
     gem "jekyll-seo-tag"
     gem "jekyll-sitemap"
     gem "jekyll-paginate"
     gem "jekyll-algolia"
   end
   ```

   Once this is done, download all dependencies by running `bundle install`.

2. Switch search providers from `lunr` to `algolia` in your `_config.yml` file:

   ```yaml
   search_provider: algolia
   ```

3. Add the following Algolia credentials to your `_config.yml` file. *If you don't have an Algolia account, you can open a free [Community plan](http://u.720life.cn/g/de5ac60d0586b8305e0a1e36246bd201ae05553e50a220e65a1dab9e909b6c204f718ef324b6b469bd870a237504740c  Once signed in, you can grab your credentials from [your dashboard](http://u.720life.cn/g/de5ac60d0586b8305e0a1e36246bd201a87d29aa88118f3a30e7f919194267893ffdeeaa61449e6fa8f65ba6f3d70f0c 

   ```yaml
   algolia:
     application_id: # YOUR_APPLICATION_ID
     index_name: # YOUR_INDEX_NAME
     search_only_api_key: # YOUR_SEARCH_ONLY_API_KEY
     powered_by: # true (default), false
   ```

4. Once your credentials are setup, you can run the indexing with the following command:

   ```
   ALGOLIA_API_KEY=your_admin_api_key bundle exec jekyll algolia
   ```

   For Windows users you will have to use `set` to assigned the `ALGOLIA_API_KEY` environment variable.

   ```
   set ALGOLIA_API_KEY=your_admin_api_key
   bundle exec jekyll algolia
   ```

   Note that `ALGOLIA_API_KEY` should be set to your admin API key.

To use the Algolia search with GitHub Pages hosted sites follow [this deployment guide](http://u.720life.cn/g/25c151d41744ac4fd0e3c488e14a36a5e2d0224b37dd845f0f2af0ea1b1248b69f99c2bc2cbe4a7cca7910e63dbad58d03daea964ee274d39dd1b8e5b4584c2a  Or this guide for [deploying on Netlify](http://u.720life.cn/g/25c151d41744ac4fd0e3c488e14a36a5e2d0224b37dd845f0f2af0ea1b1248b60fa5486821f21d4a2e4e5405bfd711c18072108f3884faac8dd6ae32626e9d03 

**Note:** The Jekyll Algolia plugin can be configured in several ways. Be sure to check out [their full documentation](http://u.720life.cn/g/25c151d41744ac4fd0e3c488e14a36a5e2d0224b37dd845f0f2af0ea1b1248b6022266659d4ddda3e2a38bfaa6fbc9db1cfb088c9a5384d4cdbc4952f00823c1  "Algolia configuration") on how to exclude files and other valuable settings.

### Author

Author information is used as meta data for post "by lines" and propagates the 
`creator` field of Twitter summary cards with the following front matter in 
`_config.yml`:

```yaml
author:
  name: John Doe
  twitter: johndoetwitter
  picture: /assets/images/johndoe.png
```

Site-wide author information can be overridden in a document's front matter in 
the same way:

```yaml
author:
  name: Jane Doe
  twitter: janedoetwitter
  picture: /assets/images/janedoe.png
```

Or by specifying a corresponding key in the document's front matter, that 
exists in `site.data.authors`. E.g., you have the following in the document's 
front matter:

```yaml
author: megaman
```

And you have the following in `_data/authors.yml`:

```yaml
megaman:
  name: Mega Man
  twitter: megamantwitter
  picture: /assets/images/megaman.png

drlight:
  name: Dr. Light
  twitter: drlighttwitter
  picture: /assets/images/drlight.png
```

Currently `author.picture` is only used in `layout: about`. Recommended size is 
`300 x 300` pixels.

### Reading Time

To enable reading time counts add `read_time: true` to a post or page's YAML 
Front Matter.

### Comments (via Disqus)

Optionally, if you have a [Disqus](http://u.720life.cn/g/27b75a4361e12b2cf69ad7924b6f91fcc319c2261de474cbca29b1b6d03a383c)  account, you can show a 
comments section below each post.

To enable Disqus comments, add your [Disqus shortname](http://u.720life.cn/g/d7a478cfbccca9c269e0e2d971a3cf1414f53d9db4a75cacf611861e3d73a6dac2a86dab4e6c4c0fd943d5d5fcb2560261ea4f9a956a5395ce96f933b8b39629)  to your project's 
`_config.yml` file:

```yaml
  disqus:
    shortname: my_disqus_shortname
```

Comments are enabled by default and will only appear in production when built 
with the following [environment value](http://u.720life.cn/g/41b49956459f45e009beb54ff3039b857a5f8372db0c8ead1ac818720c46bb5d7e2f251828b99c644b737c1221e3f12cff0748103fb69711aea255ffa293481d532cb2e5f8564d2ee2e6291b1a00ab2e8161ec73afd14561adb9c891e46a1f26  
`JEKYLL_ENV=production`

If you don't want to display comments for a particular post you can disable 
them by adding `comments: false` to that post's front matter.

### Google Analytics

To enable Google Analytics, add your [tracking ID](http://u.720life.cn/g/3f6bc38e6938b6711866a3ba7ee64d801de335b4ddc994dbe1cb2c292ea3021ac6b1699c72362bd8d75c879083a77d6dda364721582224e8f06c3ad66201eea8)  
to `_config.yml` like so:

```yaml
  google_analytics: UA-NNNNNNNN-N
```

Similar to comments, the Google Analytics tracking script will only appear in 
production when using the following environment value: `JEKYLL_ENV=production`.

### Copyright

By default the copyright line in the footer displays the current year 
(at build time) followed by your site's title. e.g. `© 2018 Basically Basic.`

If you would like to change this add `copyright` to your `_config.yml` file 
with appropriate text:

```yaml
copyright: "My custom copyright."
```

## Layouts

This theme provides the following layouts, which you can use by setting the 
`layout` [Front Matter](http://u.720life.cn/g/6a21ed45e167b1aa1cd0b5f81e69eba9d6e8d9c9bf18eb395a386a1c05d295b6b53a455c66bc683a5987d8da6eb9c9cf)  on each page, 
like so:

```yaml
---
layout: name
---
```

### `layout: default`

This layout handles all of the basic page scaffolding placing the page content 
between the masthead and footer elements. All other layouts inherit this one 
and provide additional styling and features inside of the `{{ content }}` block.

### `layout: post`

This layout accommodates the following front matter:

```yaml
# optional alternate title to replace page.title at the top of the page
alt_title: "Basically Basic"

# optional sub-title below the page title
sub_title: "The name says it all"

# optional intro text below titles, Markdown allowed
introduction: |
    Basically Basic is a Jekyll theme meant to be a substitute for the default --- [Minima](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c118f2b5609c9865ea6387ad7d5e9170797cb797c3e93a99b5813946c6160236  Conventions and features found in Minima are fully supported by **Basically Basic**.

# optional call to action links
actions:
  - label: "Learn More"
    icon: github  # references name of svg icon, see full list below
    url: "http://url-goes-here.com"
  - label: "Download"
    icon: download  # references name of svg icon, see full list below
    url: "http://url-goes-here.com"

image:  # URL to a hero image associated with the post (e.g., /assets/page-pic.jpg)

# post specific author data if different from what is set in _config.yml 
author:
  name: John Doe
  twitter: johndoetwitter

comments: false  # disable comments on this post
```

**Note:** Hero images can be overlaid with a transparent "accent" color to unify them with the theme's palette. To enable, [customize the CSS](#customizing-sass-scss) with the following Sass variable override:

```scss
$intro-image-color-overlay: true;
```

### `layout: page`

Visually this layout looks and acts the same as `layout: post`, with two minor 
differences.

- Author "by line" and publish date are omitted.
- Disqus comments are omitted.

### `layout: home`

This layout accommodates the same front matter as `layout: page`, with the 
addition of the following:

```yaml
paginate: true  # enables pagination loop, see section above for additional setup
entries_layout: # list (default), grid
```

By default, posts are shown in a list view. To change to a grid view add `entries_layout: grid` to the page's front matter.

### `layout: posts`

This layout displays all posts grouped by the year they were published. It accommodates the same front matter as `layout: page`.

By default, posts are shown in a list view. To change to a grid view add `entries_layout: grid` to the page's front matter.

### `layout: categories`

This layout displays all posts grouped category. It accommodates the same front matter as `layout: page`.

By default, posts are shown in a list view. To change to a grid view add `entries_layout: grid` to the page's front matter.

### `layout: tags`

This layout displays all posts grouped by tag. It accommodates the same front matter as `layout: page`.

By default, posts are shown in a list view. To change to a grid view add `entries_layout: grid` to the page's front matter.

### `layout: collection`

This layout displays all documents grouped by a specific collection. It accommodates the same front matter as `layout: page` with the addition of the following:

```yaml
collection: # collection name
entries_layout: # list (default), grid
show_excerpts: # true (default), false
sort_by: # date (default) title
sort_order: # forward (default), reverse
```

To create a page showing all documents in the `recipes` collection you'd create `recipes.md` in the root of your project and add this front matter:

```yaml
title: Recipes
layout: collection
permalink: /recipes/
collection: recipes
```

By default, documents are shown in a list view. To change to a grid view add `entries_layout: grid` to the page's front matter. If you want to sort the collection by title add `sort_by: title`. If you want reverse sorting, add `sort_order: reverse`.

### `layout: category`

This layout displays all posts grouped by a specific category. It accommodates the same front matter as `layout: page` with the addition of the following:

```yaml
taxonomy: # category name
entries_layout: # list (default), grid
```

By default, posts are shown in a list view. To change to a grid view add `entries_layout: grid` to the page's front matter.

To create a page showing all posts assigned to the category `foo` you'd create `foo.md` in the root of your project and add this front matter:

```yaml
title: Foo
layout: category
permalink: /categories/foo/
taxonomy: foo
```

### `layout: tag`

This layout displays all posts grouped by a specific tag. It accommodates the same front matter as `layout: page` with the addition of the following:

```yaml
taxonomy: # tag name
entries_layout: # list (default), grid
```

By default, posts are shown in a list view. To change to a grid view add `entries_layout: grid` to the page's front matter.

To create a page showing all posts assigned to the tag `foo bar` you'd create `foo-bar.md` in the root of your project and add this front matter:

```yaml
title: Foo Bar
layout: tag
permalink: /tags/foo-bar/
taxonomy: foo bar
```

### `layout: about`

This layout accommodates the same front matter as `layout: page`, with the 
addition of the following to display an author picture:

```yaml
author:
  name: John Doe
  picture: /assets/images/johndoe.png
```

Recommended `picture` size is approximately `300 x 300` pixels. If `author` 
object is not explicitly set in the about page's front matter the theme 
will default to the value set in `_config.yml`.

If blank there no image will appear.

### `layout: cv`

This layout accommodates the same front matter as `layout: page`. It 
leverages a [JSON-based file standard](http://u.720life.cn/g/d83c11b6587decf8c5b182cb7d9e5d7b31275017b78727a67e81de9ed7c8a50a)  for 
resume data to conveniently render a curriculum vitæ or resume painlessly.

Simply use JSON Resume's [in-browser resume builder](http://u.720life.cn/g/ab2bf93b726c7cfc95725d15781f717ca3baff1c8eea16e4f02fb591b8d77160)  
to export a JSON file and save to your project as `_data/cv.json`.

## Images

Suggested image sizes in pixels are as follows:

| Image | Description | Size |
| ----- | ----------- | ---- |
| `page.image.path` | Large full-width document image. | Tall images will push content down the page. `1600 x 600` is a good middle-ground size to aim for. |
| `page.image` | Short-hand for `page.image.path` when used alone (without `thumbnail`, `caption`, or other variables). | Same as `page.image.path` |
| `page.image.thumbnail` | Small document image used in grid view. | `400 x 200` |
| `author.picture` | Author page image. | `300 x 300` |

## Customization

The default structure, style, and scripts of this theme can be overridden and 
customized in the following two ways.

### Overriding Includes and Layouts

Theme defaults can be [overridden](http://u.720life.cn/g/41b49956459f45e009beb54ff3039b8565a1e19b956440c1cb98b45f012badf0f46549d962b4545fbef09d279bcbf07762f5a45b74147de434271c8879a3d27b)  
by placing a file with the same name into your project's `_includes` or 
`_layouts` directory. For instance:

- To specify a custom style path or meta data to the [`_includes/head.html `](_includes/head.html) 
file, create an `_includes` directory in your project, copy 
`_includes/head.html` from Basically Basic's gem folder to 
` /_includes` and start editing that file.

**ProTip:** to locate the theme's files on your computer run 
`bundle show jekyll-theme-basically-basic`. This returns the location of the 
gem-based theme files.

### Customizing Sass (SCSS)

To override the default [Sass](http://u.720life.cn/g/2437957cdee2b2e4308451169793ee4ea1254853bebb544ac2b45c166d0ccddc)  (located in theme's 
`_sass` directory), do one of the following:

1. Copy directly from the Basically Basic gem

   - Go to your local Basically Basic gem installation directory (run 
     `bundle show jekyll-theme-basically-basic` to get the path to it).
   - Copy the contents of `/assets/stylesheets/main.scss` from there to 
     ` `.
   - Customize what you want inside ` /assets/stylesheets/main.scss`.

2. Copy from this repo.

   - Copy the contents of [assets/stylesheets/main.scss](assets/stylesheets/main.scss) 
     to ` `.
   - Customize what you want inside ` ` due to the way Jekyll currently reads those files.

To make basic tweaks to theme's style Sass variables can be overridden by adding 
to ` /assets/stylesheets/main.scss`. For instance, to change the 
accent color used throughout the theme add the following:

```scss
$accent-color: red;
```

### Customizing JavaScript

To override the default JavaScript bundled in the theme, do one of the following:

1. Copy directly from the Basically Basic gem

   - Go to your local Basically Basic gem installation directory (run 
     `bundle show jekyll-theme-basically-basic` to get the path to it).
   - Copy the contents of `/assets/javascripts/main.js` from there to 
     ` `.
   - Customize what you want inside ` /assets/javascripts/main.js`.

2. Copy from this repo.

   - Copy the contents of [assets/javascripts/main.js](assets/javascripts/main.js) 
     to ` `.
   - Customize what you want inside ` /assets/javascripts/main.js`.

### SVG Icons

The theme uses social network logos and other iconography saved as SVGs for 
performance and flexibility. Said SVGs are located in the `_includes` directory 
and prefixed with `icon-`. Each icon has been sized and designed to fit a 
`16 x 16` viewbox and optimized with [SVGO](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304674c96a2157dd4af0ba94cfc76269ee65 

| Icon | Filename |
| --- | --- |
|   | icon-arrow-left.svg |
|   | icon-arrow-right.svg |
|   | icon-bitbucket.svg |
|   | icon-calendar.svg |
|   | icon-codepen.svg |
|   | icon-download.svg |
|   | icon-dribbble.svg |
|   | icon-email.svg |
|   | icon-facebook.svg |
|   | icon-flickr.svg |
|   | icon-github.svg |
|   | icon-gitlab.svg |
|   | icon-googleplus.svg |
|   | icon-instagram.svg |
|   | icon-lastfm.svg |
|   | icon-linkedin.svg |
|   | icon-pdf.svg |
|   | icon-pinterest.svg |
|   | icon-rss.svg |
|   | icon-soundcloud.svg |
|   | icon-stackoverflow.svg |
|   | icon-stopwatch.svg |
|   | icon-tumblr.svg |
|   | icon-twitter.svg |
|   | icon-xing.svg |
|   | icon-youtube.svg |

Fill colors are defined in the `_sass/basically-basic/_icons.scss` partial and 
set with `.icon-name` where class name matches the corresponding icon.

For example the Twitter icon is given a fill color of `#1da1f2` like so:

```html
 {% include icon-twitter.svg %} 
```

Alongside the SVG assets, there are icon helper includes to aid in generating 
social network links.

| Include Parameter | Description                      | Required                |
| ----------------- | ---------------------------------| ----------------------- |
| `username`        | Username on given social network | **Required**            |
| `label`           | Text used for hyperlink | Optional, defaults to `username` |

For example, the following `icon-github.html` include:

```liquid
{% include icon-github.html username=jekyll label='GitHub' %}
```

Will output the following HTML:

```html
 
        
   GitHub 
 
```

### Customizing Sidebar Content

---

## Development

To set up your environment to develop this theme:

1. Clone this repo
2. `cd` into `/example` and run `bundle install`.

To test the theme the locally as you make changes to it:

1. `cd` into the root folder of the repo (e.g. `jekyll-theme-basically-basic`).
2. Run `bundle exec rake preview` and open your browser to 
   `http://localhost:4000/example/`. 

This starts a Jekyll server using the theme's files and contents of the 
`example/` directory. As modifications are made, refresh your browser to see 
any changes.

## Contributing

Found a typo in the documentation? Interested in adding a feature or 
[fixing a bug][issues]? Then by all means [submit an issue][new-issue] or take a
stab at submitting a [pull request][using-pull-requests]. If this is your first 
pull request, it may be helpful to read up on the [GitHub Flow][github-flow].

[issues]: https://github.com/mmistakes/jekyll-theme-basically-basic/issues
[new-issue]: https://github.com/mmistakes/jekyll-theme-basically-basic/issues/new
[using-pull-requests]: https://help.github.com/articles/using-pull-requests/
[github-flow]: https://guides.github.com/introduction/flow/

### Pull Requests

When submitting a pull request:

1. Clone the repo.
2. Create a branch off of `master` and give it a meaningful name (e.g.
   `my-awesome-new-feature`) and describe the feature or fix.
3. Open a pull request on GitHub.

Sample pages can be found in the [`/docs`](docs) and [`/example`](/example) 
folders if you'd like to tackle any "low-hanging fruit" like fixing typos, bad 
grammar, etc.

---

## Credits

### Creator

**Michael Rose**

-  
-  
-  

### Icons + Demo Images:

- [Simple Icons](http://u.720life.cn/g/01fad17dcd7e28ae492ec1cccf28231a76724920cce80a0d3ab5111fa5c106a7) 
- [Noun Project](http://u.720life.cn/g/de31c0e366db045c07b92f29c210c37eb0417200873ecd29dfab8c6c32166443) 
- [Unsplash](http://u.720life.cn/g/ee430f85f3b2f62627f32f2cb5f8804fba8f8248e887a475195cfa67c38387d9) 

### Other:

- [Jekyll](http://u.720life.cn/g/41b49956459f45e009beb54ff3039b85f43fe19d9f117a3eb298ec6599941d64) 
- [Susy](http://u.720life.cn/g/219ed21acab2b4274fe2dab8b898cead35f995afec1352b62b9dd8f5dd7679c4) 
- [Breakpoint](http://u.720life.cn/g/0432ff5a4da3d1ca34b90c0719c542e1dad48c48bcb9de2a83677752c8ff875c) 

---

## License

The MIT License (MIT)

Copyright (c) 2017-2018 Michael Rose and contributors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

Basically Basic incorporates icons from [The Noun Project](http://u.720life.cn/g/de31c0e366db045c07b92f29c210c37e9092fcaff6ea1794b5f99974f864ed1c 
Icons are distributed under Creative Commons Attribution 3.0 United States (CC BY 3.0 US).

Basically Basic incorporates photographs from [Unsplash](http://u.720life.cn/g/ee430f85f3b2f62627f32f2cb5f8804f5abc87f6f6b221cdd7ae392a9b5a52e9 

Basically Basic incorporates [Susy](http://u.720life.cn/g/219ed21acab2b4274fe2dab8b898cead2f92bf542da380870b12025f7531b34a 
Copyright (c) 2017, Miriam Eric Suzanne.
Susy is distributed under the terms of the [BSD 3-clause "New" or "Revised" License](http://u.720life.cn/g/22e7b067064505b0b066921a690bc00f1d50276b811118d1c1385e5fc89962b8b6e21177a84b31b3e77c4d99d0ec900a 

Basically Basic incorporates [Breakpoint](http://u.720life.cn/g/0432ff5a4da3d1ca34b90c0719c542e14371dfdc3adcde0c72557b1407022a42 
Breakpoint is distributed under the terms of the [MIT/GPL Licenses](http://u.720life.cn/g/ba059582536a397f7c573b87c8bea647045b0ef049248233b6f76e909e70200f1567298d3cec1ba9db5fb143826b0c9b 



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)
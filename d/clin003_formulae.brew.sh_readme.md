# Homebrew Formulae

[Homebrew Formulae](http://u.720life.cn/g/7c7c1a248d55b55e86779aadf8b9289a15f299ab4f9f719037e0fef184e5913f)  is an online package browser for [Homebrew](http://u.720life.cn/g/0a2211bd9d9066fae8cdaf6612daaa9a30e266573a4962bb36b9bb795fbfabeb 

It displays all packages in [Homebrew/homebrew-core](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ff07b068bd0d87d4a15cfe8867140a402df6a3fe3b897031a40e8840ada546e7)  and [Homebrew/homebrew-cask](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ff07b068bd0d87d4a15cfe8867140a40060597ec9ea8c38d64a98c546ebe79fc  A GitHub Action in [homebrew-core](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ff07b068bd0d87d4a15cfe8867140a40033299021159c9a06cf7706caaab6a5f3bcc979c39a84c119cef29d718c1778933005c10ebeabf4233eb4f44ec1ce4c2)  or [homebrew-cask](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ff07b068bd0d87d4a15cfe8867140a40c6e262029f96ba91da3d89b662af554d0d42c3ef8f7e4a3c36b8e7a8ef4d73a1f4ae989e916df4920de2305011f565be)  is run on each commit, which deploys the site to GitHub Pages.

## JSON API

It also provides a JSON API for all packages (or individual packages) in [Homebrew/homebrew-core](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ff07b068bd0d87d4a15cfe8867140a402df6a3fe3b897031a40e8840ada546e7)  and their related analytics. This JSON data is used for the creation of the HTML resources on this site.

Currently available:
- List formulae metadata for all homebrew-core formulae
- Get formula metadata for a homebrew-core formula
- List analytics events
- List analytics events for all homebrew-core formulae

Read more in the [JSON API documentation](http://u.720life.cn/g/7c7c1a248d55b55e86779aadf8b9289adec2c5e61ec3b2b9e39899b979fa5cd9f3a30686d54e25311b7f92861b8c31c9 

## Usage
Open https://formulae.brew.sh/ in your web browser.

To instead run Homebrew Formulae locally, run:
```bash
git clone https://github.com/Homebrew/formulae.brew.sh
cd formulae.brew.sh
bundle install
bundle exec jekyll serve
```

## License
Code is under the [BSD 2-clause "Simplified" License](LICENSE.txt).



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)
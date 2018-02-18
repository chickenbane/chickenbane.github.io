---
title: Team Engineer
categories: docs setup
---
### Open Source, Java, Google

Thanks to GitHub I get to learn Markdown and Jekyll.

* [Mastering Markdown](https://guides.github.com/features/mastering-markdown/)
* [GitHub Pages](https://help.github.com/categories/customizing-github-pages/)
* [GitHub Slate Theme](https://github.com/pages-themes/slate)
* [Jekyll](https://jekyllrb.com/docs/home/)

### Set this up on macOS
1. install ruby in Homebrew `brew install ruby`
    * Ensure Homebrew ruby in /usr/local/bin comes before macOS /bin
2. install jekyll and bundler ruby gems `gem install jekyll bundler`
3. add Gemfile, install dependencies `bundle install`
4. build and run `bundle exec jekyll serve`
5. add _config.yml with theme
6. add Gemfile.lock and _site/ to .gitignore

[First post]({% post_url 2017-06-04-google-io-wear-2.0-complications %})

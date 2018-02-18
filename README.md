# chickenbane.github.io
pages.github.com thing, probably specific to my android adventures

# Who needs index.html
Markdown: https://guides.github.com/features/mastering-markdown/

Attempting a MarkDown link: [170604-google-io-wear-2.0-complications]
[foo]({% post_url 2017-06-04-google-io-wear-2.0-complications %})
[bar]({{ site.baseurl }}{% post_url 2017-06-04-google-io-wear-2.0-complications %})

Direct link: https://chickenbane.github.io/170604-google-io-wear-2.0-complications

# setup
* `brew install ruby`
* `gem install jekyll bundler`
* add Gemfile
* `bundle install`
* build and run `bundle exec jekyll serve`
* add _config.yml file with theme
* add Gemfile.lock and _site to .gitignore
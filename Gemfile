source "https://rubygems.org"

# GitHub Pages compatible Jekyll version
gem "jekyll", "~> 4.3.0"

# Required for GitHub Pages
gem "jekyll-feed", "~> 0.12"
gem "jekyll-sitemap"
gem "jekyll-seo-tag"

# Syntax highlighting
gem "rouge"

# Windows platform support
gem "wdm", "~> 0.1.0", :platforms => [:mingw, :x64_mingw, :mswin, :x64_mswin]

group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.12"
  gem "jekyll-sitemap"
  gem "jekyll-seo-tag"
endgroup

# Performance booster (optional)
gem "jekyll-paginate"

# Windows and JRuby does not include zoneinfo files, so bundle the tzinfo-data gem
# and associated library.
platforms :mingw, :x64_mingw, :mswin, :x64_mswin do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Lock `http_parser.rb` gem to `v0.6.x` on JRuby builds since newer versions of the gem
# do not have a Java counterpart.
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]

# frozen_string_literal: true

source "https://rubygems.org"

gem "jekyll-theme-chirpy", "~> 6.3", ">= 6.3.1"
gem "jekyll-sass-converter", "~> 2.0"

group :jekyll_plugins do
  gem "jekyll-compose"
  gem "html-proofer", "~> 4.4"
 gem "jekyll-feed"
  gem "jekyll-sitemap"
end

# Windows and JRuby does not include zoneinfo files, so bundle the tzinfo-data gem
# and associated library.
gem "tzinfo", ">= 1", "< 3", platforms: [:mingw, :x64_mingw, :mswin, :jruby]
gem "tzinfo-data", platforms: [:mingw, :x64_mingw, :mswin, :jruby]

# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.1.1", platforms: [:mingw, :x64_mingw, :mswin]

# Lock `http_parser.rb` gem to `v0.6.x` on JRuby builds since newer versions of the gem
# do not have a Java counterpart.
gem "http_parser.rb", "~> 0.6.0", platforms: [:jruby]

# Lock jekyll-sass-converter to 2.x on Linux-musl
if RUBY_PLATFORM =~ /linux-musl/
  gem "jekyll-sass-converter", "~> 2.0"
end

source "https://rubygems.org"

# The Creative theme is vendored into this repo, so we just need Jekyll itself.
# Run the site locally with:  bundle exec jekyll serve
gem "jekyll", "~> 4.3"

# Modern Jekyll plugins
group :jekyll_plugins do
  gem "jekyll-seo-tag"
  gem "jekyll-sitemap"
end

# Ruby 3.4 removed several gems from the default set; declare them so the
# site builds on both Ruby 3.1 (CI) and Ruby 3.4+ (local dev).
gem "bigdecimal"
gem "csv"
gem "base64"
gem "logger"

# Windows and JRuby do not include zoneinfo files, so bundle the tzinfo-data gem
# and associated library.
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.1", :platforms => [:mingw, :x64_mingw, :mswin]

# Lock `http_parser.rb` gem to `v0.6.x` on JRuby builds since newer versions of
# the gem do not have a Java counterpart.
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]

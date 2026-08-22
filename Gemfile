# frozen_string_literal: true

source "https://rubygems.org"

# Use the Chirpy theme gem for the site
gem "jekyll-theme-chirpy", "~> 7.6"

# Include the html-proofer for site testing
gem "html-proofer", "~> 5.0", group: :test

# Windows-specific dependencies for local development
platforms :windows, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
  gem "wdm", "~> 0.2.0"
end

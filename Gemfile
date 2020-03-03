source "https://rubygems.org"

gem "github-pages", group: :jekyll_plugins

gem "tzinfo-data"
gem "wdm", "~> 0.1.0" if Gem.win_platform?
gem "nokogiri", "~> 1.10.8"

Jekyll::Hooks.register :posts, :pre_render do |post|

  if post.data['excerpt_separator'].nil? && post.content =~ /^(<!--\s*more\s*-->)$/
    post.data["excerpt_separator"] = $1
    post.data['excerpt'] = Jekyll::Excerpt.new(post)
  end

# If you have any plugins, put them here!
group :jekyll_plugins do
  gem "jekyll-paginate"
  gem "jekyll-sitemap"
  gem "jekyll-gist"
  gem "jekyll-feed"
  gem "jemoji"
  gem "jekyll-include-cache"
  gem "jekyll-algolia"
end

# Front End Prototyping (test drive)

Based on [Made Mistakes Jekyll](https://github.com/mmistakes/made-mistakes-jekyll)

Built with [Jekyll](http://jekyllrb.com) and a starter theme called [Skinny Bones](https://github.com/mmistakes/skinny-bones-jekyll).

*Please note: this hasn't been completely "themed" like some of my other [Jekyll repos] and isn't GitHub Pages compatible. In some cases the Jekyll plugins may be safe to remove without breaking things while others may not fare as well.*

The two biggies likely to cause the most headaches are [Jekyll Archives](https://github.com/jekyll/jekyll-archives) and [Jekyll Assets](https://github.com/ixti/jekyll-assets). Archives auto-generates all of the tag pages so you'll need an alternative solution or just go without them if you turn that baby off.

Jekyll Assets is used to build, concatenate, MD5 fingerprint, and minify stylesheets and JavaScript. All of this can be done with Grunt/Gulp instead if you prefer that workflow or you could simplify things and use Jekyll to preprocess your Sass partials. Either way it's doable with minor edits.

### Plugins Used

* [Jekyll Sitemap](https://github.com/jekyll/jekyll-sitemap) (GitHub Pages supported)
* [Jekyll Archives](https://github.com/jekyll/jekyll-archives)
* [Jekyll Assets](https://github.com/ixti/jekyll-assets)
* [Jekyll Related Posts](https://github.com/jumanji27/related_posts-jekyll_plugin)

### Local Development

1. Install dependencies `bundle install`
2. Run Jekyll server to preview `bundle exec jekyll serve --config _config-dev.yml --no-watch`. Good idea to disable auto-regeneration since the site is quite large and takes a few minutes to compile.

# jekyll-octopod-bulma

jekyll-octopod-bulma is a gem-based Jekyll theme: the sidebar-layout look of
[jekyll-octopod](https://jekyll-octopod.github.io/), served straight from the gem instead of
being copied into every podcast site.

It's a fork of [jekyll-bulma](https://github.com/jekyll-octopod/jekyll-bulma) — same Bulma +
Line Awesome foundation (`_sass`, `assets/css`, `assets/js`, `assets/fonts`) — with jekyll-bulma's
generic demo layouts/includes replaced by octopod's own sidebar layout, post/feed layouts, and
vendored podcast assets (Podlove web player, podcast subscribe button, default logo/favicons).
It does not depend on the `jekyll-bulma` gem at runtime; the two diverge from this fork point on.

## Requirements

Like jekyll-bulma, this bundles Bulma 1.x, which needs
[jekyll-sass-converter](https://github.com/jekyll/jekyll-sass-converter) 3.x (Dart Sass). Older
1.x/2.x (LibSass-based) converters can't build this theme.

## Usage

Add to your site's `Gemfile`:

```ruby
gem "jekyll-octopod-bulma", "~> 0.1"
```

And in `_config.yml`:

```yaml
theme: jekyll-octopod-bulma
```

Any file your site places at the same relative path (e.g. your own `_sass/_overrides.scss`,
`assets/img/logo.jpg`) shadows the gem's copy — no per-site copy step needed for the theme itself.
See [jekyll-octopod](https://jekyll-octopod.github.io/) for the full podcast-site setup, which
supplies this theme plus the podcast-specific plugin code (feed/page generators) as a separate
gem.

## License

MIT, see [LICENSE.txt](LICENSE.txt).

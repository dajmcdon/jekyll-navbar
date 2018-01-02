# jekyll-theme-bootstrap4-navbar-cdn

I just wanted a lean Bootstrap 4 CDN based theme with navigation. For some reason I couldn't find it, so I made my own.

## Installation

Add this line to your Jekyll site's `Gemfile`:

```ruby
gem "jekyll-theme-bootstrap4-navbar-cdn"
```

And add this line to your Jekyll site's `_config.yml`:

```yaml
theme: jekyll-theme-bootstrap4-navbar-cdn
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install jekyll-theme-bootstrap4-navbar-cdn

## Usage

### Navigation
Just create your own _data/navigation.yml to owerride the default example navigation. The format looks like:
```yml
- title: Home
  url: /

- title: Contact
  url: /contact/

- title: About
  url: /about/
  sublinks:
    - title: Company
      url: /about/company/
    - title: Jobs
      url: /about/jobs/
```
This will setup your site's navigation.

### Layouts

This theeme include three layouts: default.html, page.html, post.html. Page and post inherits from default, so the only layout really is default.html. And it's simple like this:
```html
<!DOCTYPE html>
<html lang="{{ page.lang | default: site.lang | default: "en" }}">
{% include head.html %}
<body>
    {% include nav.html %}

    <div class="container" aria-label="Content">
    {{ content }}
    </div>

    {% include footer.html %}
</body>
</html>
```

### Variables

* site.lang
* site.google_analytics
* page.lang

### Includes

head.html have the links to bootstrap 4 CDN css.
nav.html is the navigation.
footer.html have the links to Bootstrap 4 CDN js files needed.

## TODO

* Add dummy pages.
* Add Disqus.
* Add favicon and icon manifests.
* EU Cookie Law.
* Twitter struff
* Github stuff

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/granbom/jekyll-bootstrap4-navbar-cdn

## License

The theme is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

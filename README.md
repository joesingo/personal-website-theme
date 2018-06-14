This repository contains a HTML template and static files to build
[joesingo.co.uk](http://joesingo.co.uk) with
[mdss](https://github.com/joesingo/mdss/tree/dev/). It is a very simple bootstrap
page that includes a navbar and breadcrumbs.

## Usage

Include this in the mdss site config:

```yaml
theme_dir: <path to the checkout of this repo>
default_template: base.html
default_context:
    sitename: <name of the website>
```

In addition to the template variables present by default in `mdss`, the
the following variables are used:

| Variable    | Description |
| ----------- | ----------- |
| extra_body  | HTML to include before the page content |
| extra_style | CSS rules to include in a `<style>` tag |
| js_scripts  | List of paths to JavaScript files to include in the `<head>` section |
| keywords    | List of keywords for the page to be included as a [schema.org](https://schema.org) property |
| sitename    | Website name to be displayed in the navbar (default: My Website) |
| stylesheets | List of paths to external stylesheets |

Note that all variables are optional. `sitename` should be set in the
`default_context` section in the mdss site config to avoid repeating it on each
page.

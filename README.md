This repository contains a HTML template and static files to build
[joesingo.co.uk](http://joesingo.co.uk) with
[mdss](https://github.com/joesingo/mdss/tree/dev/). It includes a single
default page that includes a navbar and breadcrumbs.

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
| extra_head  | HTML to include at the end of the `<head>` section |
| extra_style | CSS rules to include in a `<style>` tag |
| fa_icon     | [Font Awesome](https://fontawesome.com/) icon displayed next to the site name in the navbar (see the [list of icons](https://fontawesome.com/icons?d=gallery). (default: lemon) |
| favicon_url | URL to an `*.ico` file to use as site icon. Unfortunately this name is similar to `fa_icon` but is unrelated |
| js_scripts  | List of paths to JavaScript files to include in the `<head>` section |
| sitename    | Website name to be displayed in the navbar (default: My Website) |
| stylesheets | List of paths to external stylesheets |
| date        | Date page was created/updated, as a string in any format |

The following variables are used for [schema.org](https://schema.org) markup.
By default each page is a [Blog](https://schema.org/Blog) object.

| Variable        | Description |
| --------------- | ----------- |
| author          | Page author |
| base_url        | Root URL to the location the `mdss`-generated site will be hosted. This is used to construct an absolute URL to the page |
| keywords        | List of keywords for the page |
| schema_org_dict | A dictionary that is converted to [JSON-LD](https://developers.google.com/search/docs/guides/intro-structured-data) Schema.org markup |

Note that all variables are optional. `sitename` and `base_url` should be set
in the `default_context` section in the mdss site config to avoid repeating it
on each page.

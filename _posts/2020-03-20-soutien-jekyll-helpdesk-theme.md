---
title: Soutien Jekyll Helpdesk Theme
cta:
  - title: Contact Support
    icon: lifesaver
    url: https://themeforest.net/item/soutien-customer-support-helpdesk-jekyll-theme/23697280/support
  # - title: Learn Jekyll
  #   icon: album
  #   url: https://themeforest.net/item/soutien-customer-support-helpdesk-jekyll-theme/23697280/support
  - title: Customization Services
    icon: code
    url: https://themeforest.net/item/soutien-customer-support-helpdesk-jekyll-theme/23697280/support
---

#### Table of contents
{:.no_toc}
* TOC
{:toc}
{:.uk-list}

## Installation
Install the dependencies with [Bundler](http://bundler.io/):

```bash
bundle install
```

Run the following to generate your site:
```bash
bundle exec jekyll serve
```

You can find more on [Deployment Methods](https://jekyllrb.com/docs/deployment-methods/) page on Jekyll website.

## Build process
Install [UIkit](https://getuikit.com/) font end framework dependency via Npm:
```bash
npm install
```
Enable live browser reload with the following:
```bash
bundle exec jekyll s --livereload
```

Use the following commands to compile js scripts:
```bash
npm run dev
```
Compile and minify:
```bash
npm run build
```
### Sass
To modify the primary color, open `/_sass/theme/variables.scss` and replace the color values e.g.:

```scss
$global-primary-background:                   #3dd0ae;
```

Further style customisation can be done in the following files:
```
/_sass/theme/mixins.scss
/_sass/theme/variables.scss
/assets/css/main.scss
```

## Site and author details
Add your site and author details in `_config.yml`:

```yaml
# Site title and description
title:              Soutien
description:        Helpdesk Jekyll theme.
lang:               en

# Site subpath, e.g. /blog
baseurl:            ""

# Permalink URLs structure, for permalink style options see: https://jekyllrb.com/docs/permalinks/
permalink:          /:title/

# Site base hostname & protocol, e.g. http://example.com
url:                ""

# Site logo # e.g. logo.png, upload logo image file to /uploads/ folder
logo:               

# Default author settings
author:
    name:           Pete Seth
    title:          Lead Developer  
    avatar:         avatar-tom.png
```

## Update favicon

You can find the current favicon (favicon.png) inside the theme `/uploads/` directory, just replace it with your new favicon.

## Navigation 
Set in the main navigation links in `_data/navigation_header.yml`:

```yaml
  - title: About
    url: /about/
```

## Google Anaytics
To enable Google Anaytics, add the following lines to your Jekyll site:

```yaml
  google_analytics: UA-NNNNNNNN-N
```

Google Analytics will only appear in production, i.e., `JEKYLL_ENV=production`

## Disqus Comments
Optionally, if you have a Disqus account, you can tell Jekyll to use it to show a comments section below each post. To enable it, add the following lines to your Jekyll site:

```yaml
disqus:
    shortname: my_disqus_shortname
```

You can find out more about Disqus' shortnames [here](https://help.disqus.com/customer/portal/articles/466208).

Comments are enabled by default and will only appear in production, i.e., `JEKYLL_ENV=production`. If you don't want to display comments for a particular post you can disable them by adding `comments: false` to that post's YAML Front Matter.

## Call to Action

To add the following to a page:
{% raw %}
```yaml
{% include cta.html title="Didn't find an answer?" button_text="Contact Us" button_url="/contact/" subtitle="Get in touch with us for details on setup and additional custom services pricing" %}
```
{% endraw %}

## Contact Forms

### Formspree
Submit the form and confirm your email address at [FormSpree](https://formspree.io/). Then add the following include to a page, replacing the email address:

{% raw %}
```yaml
{% include formspree.html email="my_name@gmail.com" redirect="/thanks/" name="true" subject="true" %}
```
{% endraw %}

## Sources

- Google analytics [https://www.google.com/analytics/](https://www.google.com/analytics/)
- UIkit front end framework [https://getuikit.com/](https://getuikit.com/)
- Jekyll CML [https://jekyllrb.com/](https://jekyllrb.com/)

## Support

Customer support is provided through our Envato item [support](https://themeforest.net/item/soutien-customer-support-helpdesk-jekyll-theme/23697280/support) tab for up to six months from the purchase date and is provided Monday to Friday during the business week. We aim to answer all support requests daily, most are handled within 24h.

Please note items downloaded from Envato Elements are not supported so you will be unable to get assistance with technical questions, installation, third-party assets or direct guidance.

Before contacting support please:

- Read this documentation
- Describe your problem in detail
- Include links
- Attach screenshot
---
title: Docs Documentation Jekyll Theme
cta:
  - title: Contact Support
    icon: lifesaver
    url: https://themeforest.net/item/docs-responsive-documentation-manual-jekyll-theme/21131076/support
  # - title: Learn Jekyll
  #   icon: album
  #   url: https://themeforest.net/item/docs-responsive-documentation-manual-jekyll-theme/21131076/support
  - title: Customization Services
    icon: code
    url: https://themeforest.net/item/docs-responsive-documentation-manual-jekyll-theme/21131076/support
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
$global-primary-background:                   #05c896;
```

Further style customisation can be done in the following files:
```
/_sass/theme/mixins.scss
/_sass/theme/variables.scss
/assets/css/main.scss
```

### Hooks
There are four hook inlude files that simplify adding content or scripts in the theme locations:
- `_includes/hook-head.html`
- `_includes/hook-pre-closing-body.html`

## Site and author details
Add your site and author details in `_config.yml`:

```yaml
# Site title and description
title:              Guia
description:        Customer helpdesk Jekyll theme.
lang:               en

# Site subpath, e.g. /blog
baseurl:            ""

# Permalink URLs structure, for permalink style options see: https://jekyllrb.com/docs/permalinks/
permalink:          /:categories/:title/

# Site base hostname & protocol, e.g. http://example.com
url:                ""

# Site logo # e.g. logo.png, upload logo image file to /uploads/ folder
logo:               
  
# Default author settings
author:
    name:           Pete Seth
    title:          Lead Developer  
    avatar:         avatar-tom.png

# Author settings, displayed on post and doc pages if front matter references author name e.g. author: peter
authors:
    john:
      name:         John Brown
      title:        Support     
      avatar:       avatar-john.png
```

## Update favicon

You can find the current favicon (favicon.png) inside the theme `/uploads/` directory, just replace it with your new favicon.

## Navigation 
Set in the main navigation links in `_data/navigation_header.yml`:

```yaml
  - title: About
    url: /about/
```

To add a button to navigation use:
```yaml
  - title: Contact
    url: /contact/
    button: success
```

All available buttons:
```yaml
  - title: Changelog
    url: /contact/
    button: default

  - title: Contact
    url: /contact/
    button: primary

  - title: Changelog
    url: /contact/
    button: secondary

  - title: Changelog
    url: /contact/
    button: primary-outline
```
## Translation 
Set your language code in `_config.yml`:
```yml
lang: en
```
Theme strings can be translated in `_data/translation.yml`, copy the current English translation and paste it bellow the Eglish translation, then replace `en` with you language code that you set in `_config.yml` and translate the strings.

```yml
en:
  previous:                   "Previous"
  next:                       "Next"
  related_posts:              "Related Posts"
  written_by:                 "Written by"
  share_twitter:              "Share on Twitter"
  share_facebook:             "Share on Facebook"
  search_placeholder:         "Search for answers"
  search_no_results:          "No results found"
  mobile_nav_site:            "Menu"
  contact_name:               "Name"
  contact_email:              "Email"
  contact_subject:            "Subject"
  contact_message:            "Message"
  contact_send:               "Send"
```
## Alerts
There are four alert styles:

{% raw %}
```yaml
{% include alert.html style="primary" text="Cras at dolor eget urna varius faucibus tempus in elit." %}

{% include alert.html style="success" text="Cras at dolor eget urna varius faucibus tempus in elit." %}

{% include alert.html style="warning" text="Cras at dolor eget urna varius faucibus tempus in elit." %}

{% include alert.html style="danger" text="Cras at dolor eget urna varius faucibus tempus in elit." %}
```
{% endraw %}

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

### Kwes
Create the form at [Kwes](https://kwes.io/). Then add the following include to a page, replacing the key attribute with a one from you Kwes form:

{% raw %}
```yaml
{% include kwes.html key="00000" redirect="/thanks/" name="true" subject="true" %}
```
{% endraw %}

## Header 

To add a hero header to home and category pages add the following to `_config.yml` file:

```yaml
---
header:
  image: header.jpg
  background: "rgba(0, 0, 0, 0.5)"
  color: light
  title: How can we help you?
  subtitle:
  search: true
  ---
  ```

## Sources

- Google analytics [https://www.google.com/analytics/](https://www.google.com/analytics/)
- UIkit front end framework [https://getuikit.com/](https://getuikit.com/)
- Jekyll CML [https://jekyllrb.com/](https://jekyllrb.com/)

## Support

Customer support is provided through our Envato item [support](https://themeforest.net/item/docs-responsive-documentation-manual-jekyll-theme/21131076/support) tab for up to six months from the purchase date and is provided Monday to Friday during the business week. We aim to answer all support requests daily, most are handled within 24h.

Please note items downloaded from Envato Elements are not supported so you will be unable to get assistance with technical questions, installation, third-party assets or direct guidance.

Before contacting support please:

- Read this documentation
- Describe your problem in detail
- Include links
- Attach screenshot
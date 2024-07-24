---
title: Desk Jekyll Helpdesk Theme
cta:
  - title: Contact Support
    icon: lifesaver
    url: https://themeforest.net/item/desk-responsive-knowledge-base-faq-jekyll-theme/21117160/support
  # - title: Learn Jekyll
  #   icon: album
  #   url: https://themeforest.net/item/desk-responsive-knowledge-base-faq-jekyll-theme/21117160/support
  - title: Customization Services
    icon: code
    url: https://themeforest.net/item/desk-responsive-knowledge-base-faq-jekyll-theme/21117160/support
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
To modify the primary color, open `/assets/css/main.scss` and replace the `#d40c3c` color value:
```scss
// Primary template color
$global-primary-background: #d40c3c;
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
title:              Desk - Helpdesk Jekyll Theme
description:        Knowledge base Jekyll theme.

# Site base hostname & protocol, e.g. http://example.com
url:                "https://my-site.com"

# Site logo, image or text
brand:
  image:          logo.png # e.g. logo.png, upload logo image file to /assets/img/ folder
  text:           Desk      # if the above "logo:" image variable  is not set, this text logo is displayed instead

# Author settings
author:
  name:           John Smith
  email:          john@somewebsite.com
  website:        http://somewebsite.com
  facebook:       https://www.facebook.com/
  flickr:         https://flickr.com/
  dribbble:       https://dribbble.com/
  github:         https://github.com/
  googleplus:     https://plus.google.com/
  instagram:      https://www.instagram.com/
  linkedin:       https://www.linkedin.com/feed/
  pinterest:      https://www.pinterest.com/
  twitter:        https://twitter.com/
  vimeo:          https://vimeo.com/
  youtube:        https://www.youtube.com/

# Social share buttons
twitter_username:   username
github_username:    username
  ```

## Update favicon

You can find the current favicon (favicon.png) inside the theme `/uploads/` directory, just replace it with your new favicon.

## Navigation 
Set in the main navigation links in `_data/navigation_header.yml`:

```yaml
  - title: About
    url: /about/
```

## Home Page
To create a home page, just create a `index.md` file inside the root directory. The following is a YAML Front Matter example for a page:

```yaml
---
layout: help
title: How Can We Help You?
subtitle: Self Help Support
hero:
  background: "#ffffff"   # background color, note setting a background image below will overlay the background color
  image: ocean.jpg        # local image e.g ocean.jpg from /assets/posts/ folder or remote e.g https://source.unsplash.com/ZeXP6p7agjE
  align: top              # header image alignment e.g. top, center or bottom
  text: dark              # text color e.g. dark or light
  search: true            # enable search
category:
  columns: 3              # number of category columns; 1, 2, 3, 4
featured:
  title: Featured Articles
  tag: featured           # tag used to populate featured section on home page
---
```

Home page category boxes are added in `_data/navigation_categories.yml`, e.g.:

```yaml
- heading: Browse All Topics
  categories:
    - title: Getting Started
      desc: Get your account up and running in just few easy steps
      icon: settings

    - title: Account and Billing
      desc: Managing your account, creating new users and exporting data
      icon: credit-card
```

## Faqs
To create a faq page, just create a new page inside the root directory and add the following code in content:

{% raw %}
```yaml
{% include faqs.html %}
```
{% endraw %}

Next create faq post entries in `_faqs` folder, similar to creating posts.

## Images
To keep things more organized, add post images to `/assets/posts/` directory, and add theme images to `/assets/img/` directory.

To add an image to a post or page use the following codes: Local image from `/assets/posts/` directory:

{% raw %}
```yaml
{% include image.html img="girl.jpg" alt="Alt for image" caption="Girl on a rock" %}
```
{% endraw %}

External wide image with lightbox:

{% raw %}
```yaml
{% include image.html img="https://source.unsplash.com/TT-ROxWj9nA.jpg" lightbox="true" alt="Alt for image" caption="Image in lightbox" %}
```
{% endraw %}

## Adding table of contents to a post
Add the following code at the top of the post:

```yaml
#### Sections in this article
{:.no_toc}
* TOC
{:toc}
```

`{:.no_toc}` exludes `#### Sections` in this article title from indexing in table of contents.


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


## Sources

- Google analytics [https://www.google.com/analytics/](https://www.google.com/analytics/)
- UIkit front end framework [https://getuikit.com/](https://getuikit.com/)
- Jekyll CML [https://jekyllrb.com/](https://jekyllrb.com/)

## Support

Customer support is provided through our Envato item [support](https://themeforest.net/item/desk-responsive-knowledge-base-faq-jekyll-theme/21117160/support) tab for up to six months from the purchase date and is provided Monday to Friday during the business week. We aim to answer all support requests daily, most are handled within 24h.

Please note items downloaded from Envato Elements are not supported so you will be unable to get assistance with technical questions, installation, third-party assets or direct guidance.

Before contacting support please:

- Read this documentation
- Describe your problem in detail
- Include links
- Attach screenshot
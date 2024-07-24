---
title: Condesa Portfolio Jekyll Theme
cta:
  - title: Contact Support
    icon: lifesaver
    url: https://themeforest.net/user/unboundstudio
  # - title: Learn Jekyll
  #   icon: album
  #   url: https://themeforest.net/item/memoir-responsive-jekyll-theme-for-bloggers-writers-and-photographers/20989621/support
  - title: Customization Services
    icon: code
    url: https://themeforest.net/user/unboundstudio
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

## Setup

### Site and author details
Add your site and author details in `_config.yml`:
```yaml
# Site title and description
title: Condesa
description: Jekyll theme.

# Permalink URLs structure, for permalink style options see: https://jekyllrb.com/docs/permalinks/
permalink:          /:title/

# Site logo, image or text
logo:               # e.g. logo.png, upload logo image file to /assets/img/ folder
logo_light:         # if the above "logo:" image variable  is not set, this text logo is displayed instead

# Author settings, displayed in footer and on about page
author:
  email: info@blacompany.com
  phone: +1-800-354-3434
  address: 2030 West River St. <br> New York 52304
```

### Navigation Bar
Set in the main navigation links in `_data/navbar.yml`:
```yaml
- title: About
  url: /about/
```

### Footer

Edit copyright notice in `_config.yml`:
```yaml
footer:
  copyright:
```

Set in the navigation links in `_data/footer.yml`:
```yaml
- title: About
  url: /about/
```

### Google Analytics

To enable Google Anaytics, add the following lines to your Jekyll site:

```yaml
  google_analytics: UA-NNNNNNNN-N
```

Google Analytics will only appear in production, i.e., `JEKYLL_ENV=production`


### Contact block with Form (via FormSpree)

Submit the form and confirm your email address at [FormSpree](https://formspree.io/). Then add the following lines to contact page YAML Front Matter, replacing the email address:

```yaml
blocks:
- template: contact
  block: contact
  width: default
  title: | 
    We’d love to hear about your project.
    Reach out to [tom@studio.com](mailto:tom@studio.com)
    or call + 712 362 4002
  form:
    formspree: 8767565
    name: true
    subject: true
  address: true
  contact: true
  social: true
```

## Projects

To create a new projects post, you can create a new markdown file inside the `_projects` directory:
```yaml
---
weight: 4
title: Road Warrior
subtitle: Lorem ipsum 
desc: Lorem ipsum dolor sit amet, consetetur sadipscing tempor invidunt ut labore
  et dolore magna aliquyam erat
background: secondary
color: light
image: https://via.placeholder.com/1600x800
navbar:
  color: light

header:
  overlay: rgba(0,0,0, .55)
  height: full

blocks:
- template: text
  block: text
  width: xsmall
  height: full
  title: Continually promote strategic relationships via compelling best practices. Completely transition business process. 
  content:

- template: image
  block: image
  width: default
  # height: full
  columns: 2
  images:
  - https://via.placeholder.com/800x600
  - https://via.placeholder.com/600x800
  - https://via.placeholder.com/600x950
  - https://via.placeholder.com/600x600

- template: text
  block: text
  width: xsmall
  height: full
  title: Completely transition admin business process
  content: | 
    Rapidiously enable backward-compatible portals without interactive web services. 
    Monotonectally facilitate visionary total linkage for distributed e-markets. Conveniently promote equity invested ROI whereas empowered platforms. Dramatically administrate business methodologies and cross-media metrics. Intrinsicly engineer out-of-the-box leadership skills without virtual portals.

    Intrinsicly promote client-focused schemas for visionary e-services. Enthusiastically pontificate an expanded array of e-commerce whereas value-added partnerships. Continually incubate seamless models and pandemic niche markets. Seamlessly orchestrate parallel applications whereas focused metrics dompetently redefine customized relationships.

- template: content
  block: content
  width: default
---
```

The block section can be rearanged or repeated with different content.

### Adding images
To add an image to a post or page use the following frontmatter to a page:

{% raw %}
```yaml
---
blocks: 
  - template: image
    block: image
    width: default
    # height: full
    columns: 2
    images:
    - https://via.placeholder.com/800x600
    - https://via.placeholder.com/600x800
    - https://via.placeholder.com/600x950
    - https://via.placeholder.com/600x600
---
```
{% endraw %}


### Responsive Videos
Embed local videos:
```html
<video controls playsinline uk-video>
    <source src="http://www.quirksmode.org/html5/videos/big_buck_bunny.mp4" type="video/mp4">
    <source src="http://www.quirksmode.org/html5/videos/big_buck_bunny.ogv" type="video/ogg">
</video>
```
Embed YouTube videos:
```html
<iframe src="http://www.youtube.com/embed/YE7VzlLtp-4?autoplay=0&amp;showinfo=0&amp;rel=0&amp;modestbranding=1&amp;playsinline=1" width="600" height="340" frameborder="0" allowfullscreen uk-responsive></iframe>
```

To create a draft page, create the page file under the `_drafts` directory, and you can find more information in [Working with Drafts](https://jekyllrb.com/docs/drafts/).

## Pages

To create a new page, just create a new markdown file inside the root directory. The following is a YAML Front Matter example for a page:

```yaml
---
layout: blocks
title: Condesa
background: secondary # muted, #354654
color: light

navbar: 
  color: light
blocks:
- template: projects
  block: projects
  width: default

- template: cta
  block: cta
  width: xsmall
  height: full
  style: muted
  title: Start a project
  content: | 
    Dramatically transform corporate solutions and cooperative methods of empowerment. Globally engineer web-enabled testing procedures.
  button:
    text: Contact Us
    url: /contact/
---
```

## Customization

To modify the primary color, open `/assets/css/main.scss` and replace the `#d63241` color value:
```scss
// Primary template color
$global-primary-background: #d63241;
```

Further style customisation can be done in the following files:
```
/_sass/theme/mixins.scss
/_sass/theme/variables.scss
/assets/css/main.scss
```

## Development

Install [UIkit](https://getuikit.com/) font end framework dependency via Npm:
```bash
npm install
```
Enable live browser reload with the following:
```bash
bundle exec jekyll s --livereload
```

## Support

Customer support is provided through our Envato item [support](https://themeforest.net/user/unboundstudio) tab for up to six months from the purchase date and is provided Monday to Friday during the business week. We aim to answer all support requests daily, most are handled within 24h.

Please note items downloaded from Envato Elements are not supported so you will be unable to get assistance with technical questions, installation, third-party assets or direct guidance.

Before contacting support please:

- Read this documentation
- Describe your problem in detail
- Include links
- Attach screenshot
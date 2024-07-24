---
title: Étoile Writer & Blogger Jekyll Theme
cta:
  - title: Contact Support
    icon: lifesaver
    url: https://themeforest.net/item/toile-responsive-jekyll-theme-for-bloggers-and-writers/23079570/support
  # - title: Learn Jekyll
  #   icon: album
  #   url: https://themeforest.net/item/toile-responsive-jekyll-theme-for-bloggers-and-writers/23079570/support
  - title: Customization Services
    icon: code
    url: https://themeforest.net/item/toile-responsive-jekyll-theme-for-bloggers-and-writers/23079570/support
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
$global-primary-background:                   #de7a93;
```

Further style customisation can be done in the following files:
```
/_sass/theme/mixins.scss
/_sass/theme/variables.scss
/assets/css/main.scss
```

## Authors
Create an author collection post in `_authors` folder:

```yaml
---
title:          John Nolten
username:       john
default:        true
image:          https://pbs.twimg.com/profile_images/974603248119222272/N5PLzyan.jpg
bio:            Writer at WorkBox Publishing, parent, aminal lover and avid coffee drinker.
email:          me@mysite.com
website:        https://mysite.com
facebook:       https://www.facebook.com/
flickr:         https://www.flickr.com/
dribbble:       https://dribbble.com/
github:         https://github.com/
reddit:         https://www.reddit.com/
instagram:      https://www.instagram.com/
linkedin:       https://www.linkedin.com/
pinterest:      https://www.pinterest.com
twitter:        https://twitter.com/
vimeo:          https://vimeo.com/
youtube:        https://www.youtube.com/
---
```

## Widgets

Set in the page sidebar and footer sidebar widgets in `_data/sidebars.yml`. Chose from the following widgets: `categories`, `recent`, `authors`, `about`, `links`. 

Edit copyright notice in about widget in `_config.yml`:

```yaml
footer:
    copyright:
```

## Update favicon

You can find the current favicon (favicon.png) inside the theme `/uploads/` directory, just replace it with your new favicon.

## Navigation 
Set in the main navigation links in `_data/navigation_header.yml`:

```yaml
  - title: About
    url: /about/
```

## Adding images to posts
To add an image to a post or page use the following codes: Local image from `/uploads/` directory:

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

## Posts
The following post front matter variables are available:

```yaml
---
title: Best tech companies to work for in 2019
image: post-image.jpg       # Upload the image to uploads directory
categories: [business]      # Same as category post tag
tag: [spotlight, featured]  # Optional: spotlight tag adds post to spotlight section, featured tag add post to featured section
hidden: true                # Optional: exlude the post from blog page posts
author: sarah               # Reference author username
---
```

## Categories
To create a category, create a new post inside the `_category` directory and add the following YAML Front Matter:

```yaml
---
tag: business
permalink: "/category/business/"
---
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

## Contact Form

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

Customer support is provided through our Envato item [support](https://themeforest.net/item/toile-responsive-jekyll-theme-for-bloggers-and-writers/23079570/support) tab for up to six months from the purchase date and is provided Monday to Friday during the business week. We aim to answer all support requests daily, most are handled within 24h.

Please note items downloaded from Envato Elements are not supported so you will be unable to get assistance with technical questions, installation, third-party assets or direct guidance.

Before contacting support please:

- Read this documentation
- Describe your problem in detail
- Include links
- Attach screenshot
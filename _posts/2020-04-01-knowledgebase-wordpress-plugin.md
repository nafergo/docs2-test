---
title: Knowledge Base WordPress Plugin
cta:
  - title: Contact Support
    icon: lifesaver
    url: https://codecanyon.net/item/knowledge-base-helpdesk-wiki-wordpress-plugin/5758910/support
  # - title: Learn Jekyll
  #   icon: album
  #   url: https://codecanyon.net/item/knowledge-base-helpdesk-wiki-wordpress-plugin/5758910/support
  - title: Customization Services
    icon: code
    url: https://codecanyon.net/item/knowledge-base-helpdesk-wiki-wordpress-plugin/5758910/support
---

#### Table of contents
{:.no_toc}
* TOC
{:toc}
{:.uk-list}

## Installation

### File Structure
Extract (Unzip) the plugin download package. Within the download package you'll find the following file structure and contents:

- `DOCUMENTATION.html` User Documentation
- `pressapps-­knowledge­-base.zip` Installable plugin zip file
- `pressapps-­knowledge­-base` Plugin folder for FTP upload
- `import` Folder containing demo content XML import file
- `theme` Folder containing installable demo theme zip


### WordPress Installation
1. Go to `P​lugins > Add New​`.
2. Under `U​pload`,​ click `B​rowse`,​locate ​`pressapps­-knowledge-­base.zip` ​in your plugin download package and click `Open`.
3. Find the WordPress Plugin you wish to install.
4. Click `I​nstall Now​` to install the WordPress Plugin.
5. A pop up window will ask you to confirm your wish to install the Plugin.
6. Click `P​roceed​` to continue with the installation. The resulting installation screen will
list the installation as successful or note any problems during the install.
7. If successful, click `​Activate Plugin`​ to activate it.

### FTP Installation
1. Using a FTP software, upload the `pressapps-­knowledge­-base` folder located in your plugin download package to `plugins` folder on your server.
2. Go to `Plugins` screen and find the newly uploaded `P​ressApps Knowledge Base` plugin in the list.
3. Click `A​ctivate Plugin`​ to activate it.

## Setup

### Creating Knowledge Base Articles
To create a Knowledge Base posts go to `K​nowledge Base > Add New​`, enter title, post content and click Publish button to save. Knowledge Base plugin best displays posts grouped into categories. T​ags​ can also be assigned to posts. Create categories under `K​nowledge Base > Categories`​ and assign post to these categories.

{% include image.html img="Add_New_Article.png" alt="Add New Article" %}

### Setting Up Main Knowledge Base Page
There are two options to display the main knowledge base content, using Gutenberg blocks (recommended) or shortcodes.

#### Gutenberg Blocks
This requires WordPress version 5 or above. Create a page under `P​ages > Add New​`, then the plus icon to add the `Knowledge Base` block and optional search or widget area blocks and save the page.

{% include image.html img="gutenberg_blocks.png" alt="Gutenberg blocks" %}

#### Shortcode
Create a page under `P​ages > Add New​`, then add `[pakb_knowledgebase]` shortcode to its content. Optional `[pakb_search]` shortcode can be used to display search. See shortcodes section for a complete list of shortcodes and their attributes. 

### Horizontal Widget Area
Displays a horizontal widget area on the main knowledge base page, widgets can be added under ​`Appearance > Widgets`. Add the widget area to a page using Gutenberg blocks + button.

### Theme Sidebars
The plugin displays it content by overriding theme’s page template content, by default the plugin overrides `page.php` template file. If your theme has additional page templates, for example full width page template you can select the template under `Knowledge Base > General > Page Template` a​nd knowledge base plugin will use this template for its pages.

### Plugin Options
Plugin options settings are located under `Knowledge Base` menu in dashboard. ​

### Drag & Drop Knowledge Base Reorder
Navigate to `Knowledge Base > General`​ and set `Content Order` setting to `Drag and Drop`. Now you can reorder knowledge base posts and categories using drag and drop under `K​nowledge Base > All Articles` and `K​nowledge Base > Categories`. ​

### Article Voting
Allow users to leave feedback on articles by displaying Like / Dislike voting button under each content on single article page. Enable voting under `Knowledge Base > Voting`. Vote counts for each article can be found under `​Knowledge Base > All Knowledge Base` page.

### Shortcodes

#### Display List Of Knowledge Base Articles
`[pakb_articles posts_per_page="10" orderby="date" order="DESC"]`

| Option | Description | Choices | Default |
| --- | --- | --- | --- |
| posts_per_page | Number of articles to show | integer | 10 |
| orderby | Sort articles by ID, title, date, drag & drop reorder, likes| ID, title, date, menu_order | meta_value_num |
| order | Designates the ascending or descending order of the articles | ASC, DESC | DESC |
| filter | Filter by tag or category | tag, category |
| category | Category ID for category filter |integer |
| tag | Tag ID for tag filter |integer |

#### Display List Of Knowledge Base Categories
`[pakb_categories count="true" orderby="name" order="ASC" number="5"]`

| Option | Description | Choices | Default |
| --- | --- | --- | --- |
| number | Number of categories to show | integer | 10 |
| orderby | Sort categories by name or drag & drop reorder| name, term_group | name |
| order | Designates the ascending or descending order of the categories | ASC, DESC | ASC |
| count | Display article count | true, false | false |

#### Display Knowledge Base main Page
`[pakb_knowledgebase]`

#### Display Search
`[pakb_search]`

#### Display Attachments
`[pakb_attachments]`
Add to a knowledge base article that contain file attachments. Instead of using this shortcode display of attachments can be enabled globally for all articles in plugin options under `Knowledge Base > Single` page. 

### Adding Knowledge Base Widgets
Plugin has three widgets: ​Knowledge Base Search, Knowledge Base Categories​ and Knowledge Base Articles.​ To setup a widgets navigate to ​`Appearance > Widgets`​ and use the drag and drop interface to drop the widget into the desired theme sidebar area.

## Translation

The plugin is translation ready, please follow the steps bellow:

1. Download and install [Poedit](https://poedit.net/)
2. Open the program after the installation. Click **File > Open** and find the original
`pressapps-­knowledge­-base.po` ​file located in the `l​anguages`​ directory in plugin
root.
3. Translate all the words to your language and save your translated file in the same
`languages`​ directory with the name of your language and country codes.
4. If your language is, for example, Russian and the country is Russia, then you must save the file like
this: `​pressapps-­knowledge­-base­-ru_RU.po`. ​Use `pressapps-­knowledge­-base­`​, then the first parameter is a language code, the second parameter is a country code. All languages codes can be found [here](http://www.gnu.org/software/gettext/manual/gettext.html#Language-Codes).
and all countries codes can be found [here](http://www.gnu.org/software/gettext/manual/gettext.html#Country-Codes).

## Customization


### Action Hooks
`pakb_archive_loop` - action for archive page inside the loop

`pakb_category_loop` - action for category page inside the loop

`pakb_search_loop` - action for search inside the loop

`pakb_single_loop` - action for single page inside the loop

### Conditional Tags
The conditional tags can be used in your template files to change what content is displayed on a particular page.

#### Category KB Page
`is_pakb_category()` - Check if the category KB page is being displayed, returns `true / false`.

#### Single KB Page
`is_pakb_single()` - Check if the single KB page is being displayed, returns `true / false`.

#### Example
```
if ( is_pakb_category() ) {
	// Category KB page
} elseif ( is_pakb_single() ) {
	// Single KB page
}
```

## Sidebar Addon

Contextual sidebar addon allows customers to access all knowledge base articles anywhere on the site without reloading the page. We have also added Contact form 7 integration. The addon is a separate [purchase here](https://codecanyon.net/item/pressapps-knowledge-base-contextual-sidebar-addon/21091013).

### Setup
The addon will automatically display sidebar toggle button on your site after plugin activation with the default settings. Additional addon options settings are located under `Knowledge Base > Sidebar`. 

The site front end will display sidebar toggle button at the bottom right corner.

{% include image.html img="sidebar.png" alt="Sidebar Toggle Button" %}

### Contact Form
To add a contact form to the sidebar install and activate third-party plugin [Contact Form 7](https://wordpress.org/plugins/contact-form-7/).

Next, navigate to Contact menu and copy the form shortcode e.g. `[contact-form-7 id="1040"]`.

Next, navigate to `Knowledge Base > Sidebar` and paste the shortcode inside the Contact Button Shortcode textarea and save settings.

On the front end, open the sidebar and click on Contact button to reveal the form.

### Translation
1. Download and install [Poedit](https://poedit.net/)
2. Open the program after the installation. Click **File > Open** and find the original
`pressapps-­knowledge­-base-sidebar.po` ​file located in the `l​anguages`​ directory in plugin
root.
3. Translate all the words to your language and save your translated file in the same
`languages`​ directory with the name of your language and country codes.
4. If your language is, for example, Russian and the country is Russia, then you must save the file like
this: `​pressapps-­knowledge­-base­-sidebar-ru_RU.po`. ​Use `pressapps-­knowledge­-base­-sidebar`​, then the first parameter is a language code, the second parameter is a country code. All languages codes can be found [here](http://www.gnu.org/software/gettext/manual/gettext.html#Language-Codes).
and all countries codes can be found [here](http://www.gnu.org/software/gettext/manual/gettext.html#Country-Codes).


## Product Support

Support is only provided through item support tab on Codecanyon.

Please note items downloaded from Envato Elements are not supported so you will be unable to get assistance with technical questions, installation, third-party assets or direct guidance.

Before contacting support please:

- Read this documentation
- Perform basic troubleshooting by disabling plugins and switching to default theme
to identify possible cause
- Describe your problem in detail
- Include links
- Attach screenshot
- Include your WP and FTP login where appropriate

## Credits and Sources

- [UIkit](https://getuikit.com/) front end framework 

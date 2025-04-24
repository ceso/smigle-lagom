# Smigle Lite

![GitHub Actions Workflow Status](https://img.shields.io/github/actions/workflow/status/joe-mccarthy/smigle-lite/deploy-example.yml?branch=main&cacheSeconds=1&style=for-the-badge)
![Sonar Quality Gate](https://img.shields.io/sonar/quality_gate/joe-mccarthy_smigle-lite?server=https%3A%2F%2Fsonarcloud.io&cacheSeconds=1&style=for-the-badge)
![GitHub Release](https://img.shields.io/github/v/release/joe-mccarthy/smigle-lite?sort=semver&cacheSeconds=1&style=for-the-badge)
![GitHub commits since latest release](https://img.shields.io/github/commits-since/joe-mccarthy/smigle-lite/latest?cacheSeconds=1&style=for-the-badge)
![GitHub License](https://img.shields.io/github/license/joe-mccarthy/smigle-lite?cacheSeconds=1&style=for-the-badge)

## Overview

Smigle Lite is a minimalist Hugo theme focused on simplicity, performance, and privacy. It was created as a streamlined alternative to the original [Smigle](https://gitlab.com/ian-s-mcb/smigle-hugo-theme) theme, removing unnecessary elements while maintaining the core principles of being lightweight with no JavaScript or tracking.

### Core Principles

* **No JavaScript** - Pure HTML and CSS for maximum performance
* **No Tracking** - No Google analytics, cookies, or any user tracking
* **No External Dependencies** - No external fonts, comment sections, or CDN resources
* **Minimal Design** - Focus on content without distractions

## Features

### Key Differences from Original Smigle

Smigle Lite streamlines the original theme by:

* Removing the user profile image requirement
* Eliminating the site tagline
* Removing reading time estimates
* Removing word count displays
* Simplifying post metadata presentation
* Redesigning taxonomy pages as simple lists with counts
* Updating the footer with proper attributions
* Various spacing improvements and CSS optimizations
* Post Navigations
* Recent Posts displayed on each post configurable in the config file

### Theme Structure

```
smigle-lite/
├── archetypes/         # Template files for new content
├── assets/             # CSS and other asset files
├── exampleSite/        # Demo site with example content
├── i18n/               # Internationalization files
├── layouts/            # Hugo template files
└── static/             # Static files (images, etc.)
```

## Installation

### As a Git Submodule (Recommended)

From the root of your Hugo site:

```bash
git submodule add https://github.com/joe-mccarthy/smigle-lite themes/smigle-lite
```

Then, update your site's configuration file to use the theme:

```yaml
# config.yaml
theme: smigle-lite
```

Or for TOML:

```toml
# config.toml
theme = "smigle-lite"
```

### Direct Download

1. Download the [latest release](https://github.com/joe-mccarthy/smigle-lite/releases/latest)
2. Extract into your site's `themes` directory
3. Update your site's configuration file as shown above

## Quick Start Guide

### Creating a New Site with Smigle Lite

```bash
# Create a new Hugo site
hugo new site mysite -f yaml
cd mysite

# Add theme
git init
git submodule add https://github.com/joe-mccarthy/smigle-lite themes/smigle-lite

# Edit config.yaml to set theme: smigle-lite
echo 'theme: smigle-lite' >> config.yaml

# Create a new post
hugo new content/posts/my-first-post.md

# Start development server
hugo server
```

### Running the Example Site

To see a demo of the theme:

```bash
git clone https://github.com/joe-mccarthy/smigle-lite
cd smigle-lite/exampleSite
hugo server --themesDir ../..
```

Then visit [http://localhost:1313](http://localhost:1313) in your browser.

## Configuration Reference

### Basic Configuration

```yaml
# config.yaml
baseURL: "https://example.com/"
languageCode: "en-us"
title: "My Smigle Lite Site"
theme: "smigle-lite"

# Main menu configuration
menu:
  main:
    - identifier: "home"
      name: "Home"
      url: "/"
      weight: 1
    - identifier: "posts"
      name: "Posts"
      url: "/posts/"
      weight: 2
    - identifier: "categories"
      name: "Categories"
      url: "/categories/"
      weight: 3
    - identifier: "tags"
      name: "Tags"
      url: "/tags/"
      weight: 4
    - identifier: "about"
      name: "About"
      url: "/about/"
      weight: 5
```

### Theme Parameters

```yaml
# Complete theme parameters
params:
  # Latest posts section
  latest: 
    enable: true  # Enable/disable latest posts section
    count: 5      # Number of posts to display
  
  # Date formats
  abbrDateFmt: "Jan 2"  # Abbreviated date format (for lists)
  dateFmt: "January 2, 2006"  # Long date format (for post meta)
  
  # Social links in footer
  social:
    - name: "GitHub"
      url: "https://github.com/yourusername"
    - name: "Twitter"
      url: "https://twitter.com/yourusername"
    - name: "LinkedIn"
      url: "https://linkedin.com/in/yourusername"
  
  # Content license (optional)
  license:
    name: "CC BY-SA 4.0"
    url: "https://creativecommons.org/licenses/by-sa/4.0/"
    
  # Other options
  showTaxonomyLinks: true  # Show categories and tags links in post meta
  favicon: "/favicon.ico"  # Path to favicon (relative to static folder)
```

## Customization

### Custom CSS

To add your own CSS customizations, create a file at `assets/css/custom.css` in your site root. This will be automatically included.

Example custom CSS:

```css
/* assets/css/custom.css */
body {
  font-family: 'Your Preferred Font', sans-serif;
}

.site-header {
  background-color: #f0f0f0;
}
```

### Content Organization

Smigle Lite works best with the following content structure:

```
content/
├── posts/           # Blog posts
├── pages/           # Static pages
└── about/           # About page
    └── index.md
```

### Front Matter Options

```yaml
---
title: "My Post Title"
date: 2023-07-15T10:00:00-05:00
draft: false
categories: ["Technology"]
tags: ["hugo", "tutorial"]
summary: "Optional summary that will be displayed in lists"
---
```

## Advanced Usage

### Custom Shortcodes

Smigle Lite supports all built-in Hugo shortcodes plus any you create in your site's `layouts/shortcodes` directory.

### Image Handling

For responsive images:

```markdown
{{< figure src="/images/my-image.jpg" title="Image Title" alt="Image description" >}}
```

### Taxonomies

Customize how taxonomies are displayed by editing your site's configuration:

```yaml
taxonomies:
  category: categories
  tag: tags
  series: series
```

## Updating the Theme

To update the theme when used as a git submodule:

```bash
git submodule update --remote --merge
```

Or for all submodules:

```bash
git submodule foreach git pull origin main
```

## Troubleshooting

### Common Issues

1. **Theme not loading**: Ensure your `config.yaml` has `theme: smigle-lite` (or `theme = "smigle-lite"` in TOML)

2. **Styling problems**: Check for CSS conflicts with custom CSS

3. **Missing content**: Verify your content is not marked as `draft: true` unless using the `--buildDrafts` flag

## Contributing

Contributions to Smigle Lite are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request

Before submitting your PR, please:
- Ensure your code follows the project's style
- Test your changes thoroughly
- Update documentation as needed

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

* [Ian S. McBride](https://gitlab.com/ian-s-mcb) - Author and maintainer of the Hugo [Smigle](https://gitlab.com/ian-s-mcb/smigle-hugo-theme) theme
* [colorchestra](https://github.com/colorchestra) - Maintainer of [smol](https://github.com/colorchestra/smol) theme
* [Hugo](https://gohugo.io/) - The static site generator that makes this all possible

## Version History

See the [Releases](https://github.com/joe-mccarthy/smigle-lite/releases) page for the changelog and version history.

# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.2.0] - 2024-10-14

### Added

- [#4](https://github.com/joe-mccarthy/smigle-lite/issues/4) adding darkmode support
- Added option to turn off in post pagination
- Within post pagination use post title or just next/previous

### Fixed

- [#5](https://github.com/joe-mccarthy/smigle-lite/issues/5) make menu links absolute

### Removed

- [#6](https://github.com/joe-mccarthy/smigle-lite/issues/6) body text is no longer justified

## [1.1.1] - 2024-09-05

### Fixed

- header left margin when on mobile and desktop
- removed rest.css to be single css and some commented out statements

## [1.1.0] - 2024-08-25

### Added

- Added commits since last release badge to readme

### Changed

- Readme Typo
- Changelog updates
- [#1](https://github.com/joe-mccarthy/smigle-lite/issues/1) tag and category links to be absolute

### Removed

- Removed commit since last release badge

## [1.0.1] - 2024-08-23

### Changed

- Added badge to readme for build status.
- Updated github links for new repository location and name.

## [1.0.0] - 2024-08-23

- Updated readme badges for new version and updated changelog.
- updated the example site to show how to use sections and demo recursion.
- Fixed the spacing between footnotes to match rest of the theme and not overlap on mobile.
- Updated the latest posts title to be H3 rather than H1.
- updated the site header to no longer be a H1 tag to help with SEO. Style remains the same as H1.
- Post listing is now recursive for better organisation of content.
- Post navigation at the bottom of the current post to move to the next and previous post using post title.
- Added meta tags for pages, default from config, added examples of this in example-site with details for adding data to tags and categories.
- Updated category and tag post pages to allow a description to be added to the top of the listed posts. Updated the example site to show examples of this.
- This CHANGELOG file
- Added badges to the README
- Adding an example-site show that the theme can be tested before applying to site.
- Adding styling for footnotes within the text to add brackets around the number as well as remove the text decoration.
- Added configuration for site content license information in the footer. If none provided then no license information is outputted. License link now opens in new tab.
- removed social example reference to codeberg from the example-config.yaml
- Removed the example-config.yaml from the root, as there is now an example-site
- Updated Readme on how to configure the latest post section
- Social links in the footer now open in a new tab.
- Updated Readme to add information on license configuration.
- Fixed some typos in the README
- Default to not enabled, and if enabled without a post count, then default post count is set to three.
- Fixed latest posts to not include the currently viewed post.
- Last 5 published posts at the bottom of content.
- Footer to state theme being used and links back to smigle and smol
- Spacing on elements after removal of elements
- Removed the need for a user profile image.
- Removed the need for a site tag line.
- Removed the time to read post.
- Removed the word count on posts.
- Removed styling on taxonomies pages

[unreleased]: https://github.com/joe-mccarthy/smigle-lite/compare/1.2.0...HEAD
[1.2.0]: https://github.com/joe-mccarthy/smigle-lite/compare/1.1.1...1.2.0
[1.1.1]: https://github.com/joe-mccarthy/smigle-lite/compare/1.1.0...1.1.1
[1.1.0]: https://github.com/joe-mccarthy/smigle-lite/compare/1.0.1...1.1.0
[1.0.1]: https://github.com/joe-mccarthy/smigle-lite/compare/1.0.0...1.0.1
[1.0.0]: https://github.com/joe-mccarthy/smigle-lite/releases/tag/1.0.0

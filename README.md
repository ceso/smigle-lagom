# Smigle Lite

![GitHub Actions Workflow Status](https://img.shields.io/github/actions/workflow/status/joe-mccarthy/smigle-lite/deploy-example.yml?branch=main&cacheSeconds=1)
![Sonar Quality Gate](https://img.shields.io/sonar/quality_gate/joe-mccarthy_smigle-lite?server=https%3A%2F%2Fsonarcloud.io&cacheSeconds=1)
![GitHub Release](https://img.shields.io/github/v/release/joe-mccarthy/smigle-lite?sort=semver&cacheSeconds=1)
![GitHub commits since latest release](https://img.shields.io/github/commits-since/joe-mccarthy/smigle-lite/latest?cacheSeconds=1)
![GitHub License](https://img.shields.io/github/license/joe-mccarthy/smigle-lite?cacheSeconds=1)

My own site was using the [Smigle](https://gitlab.com/ian-s-mcb/smigle-hugo-theme) as I really like the concept of simplicity, lite weight with no javascript and tracking. However there were aspects that I didn't like. I found myself making far more CSS hacks than I would like. Therefore took the decision to create a new version of the theme with the changes included.

## Description

On the face of it, there isn't many changes from [Smigle](https://gitlab.com/ian-s-mcb/smigle-hugo-theme), however the changes I've made are as follows:

* Removed the need for a user profile image.
* Removed the site tag line, I'm not cool enough for one of those.
* Removed the time to read post.
* Removed the word count of posts.
* Stripped down the post meta data listings.
* Updated the taxonomies pages to just be lists with a count, no additional styles.
* Updated the footer to include a reference back to [Smigle](https://gitlab.com/ian-s-mcb/smigle-hugo-theme) and [smol](https://github.com/colorchestra/smol).
* Various spacing changes and CSS tweaks to address the removal of elements.

This theme still retains the concept of the previous two themes of which it's based:

* No JavaScript
* No Google spyware or tracking of any kind
* No other external dependencies, embedded fonts or comment sections

## Getting Started

From the root of your site:

```bash
git submodule add https://github.com/joe-mccarthy/smigle-lite themes/smigle-lite
```

### Running the example-site

To try out the theme prior to changing your site to use the theme, you can start up the example site within the theme.

```bash
git clone https://github.com/joe-mccarthy/smigle-lite
cd example-site
hugo server --source . --themesDir ../../ --theme smigle-lite
```

Open your web browser to [http://localhost:1313](http://localhost:1313) to view the demo of the theme.

### Updating

From the root of your site:

```bash
git submodule foreach git pull origin main
```

### Run example site

```bash
hugo new site mysite -f yaml
cd mysite
git init
git submodule add https://github.com/joe-mccarthy/smigle-lite themes/smigle-lite
# update config.yaml theme variable to be theme: smigle-lite
hugo server
```

### Configuration

The example-site has a configuration that shows the following:

* menu:main :- Example on how to set the menu items at the top of the site.
* params:latest :- how to enable the latest posts at the bottom of post content, and the number of posts to show.
params:abbrDateFmt :- This is the format for short date formats this is used within the /posts to show all posts by year.
* params:dateFmt :- The format of the data shown in the post meta sections.
* params:social :- List of links to be displayed in the footer of the site. This is a key value pair, with the __name__, and __url__ to navigate to.
* params:license :- configures if a license is presented in the footer for the site contents. If no license do not include this configuration item. If there is a license then two sub items have to be added for the __name__ and __url__.

## Contributing

Have you found a bug or got an idea for a new feature? Feel free to use the [issue tracker](https://github.com/joe-mccarthy/smigle-lite/issues) to let me know. Or make directly a [pull request](https://github.com/joe-mccarthy/smigle-lite/pulls).

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

* [Ian S. McBride](https://gitlab.com/ian-s-mcb) : The author and maintainer of the Hugo [Smigle](https://gitlab.com/ian-s-mcb/smigle-hugo-theme) Theme of which this theme is based upon.
* [colorchestra](https://github.com/colorchestra) : Maintainer of [smol](https://github.com/colorchestra/smol) of which [Smigle](https://gitlab.com/ian-s-mcb/smigle-hugo-theme) was derived.
* [Hugo](https://gohugo.io/) the static site generator that makes this all possible.

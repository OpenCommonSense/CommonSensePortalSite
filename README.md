# Commonsense Reasoning 

## Getting Started

### Prerequisites
1. Install [`Jekyll`](https://jekyllrb.com/docs/installation/).
2. Install [`Ruby`](https://www.ruby-lang.org/en/documentation/installation/). 
3. Install [`Bundler`](https://bundler.io). 


### Testing your GitHub Pages site locally with Jekyll
1. Open Terminal.
2. `clone` the repository and `cd` into it.
3. Run the Jekyll site locally.
      ```
        $ bundle exec jekyll serve --config _config_local.yml
        > Configuration file: _config_local.yml
        >            Source: /Users/xiaoyanq/inkLab/commonsense-run.github.io
        >       Destination: /Users/xiaoyanq/inkLab/commonsense-run.github.io/_site
        > Incremental build: disabled. Enable with --incremental
        >      Generating...
        >                    done in 0.309 seconds.
        > Auto-regeneration: enabled for '/Users/xiaoyanq/inkLab/commonsense-run.github.io'
        >    Server address: http://127.0.0.1:4000/
        >  Server running... press ctrl-c to stop.
      ```
4. To preview your site, in your web browser, navigate to `http://localhost:4000`.


## Adding a new page to your site
1. `cd` into the repository.
2. `cd` into the `docs` folder.
3. In the `docs` folder, create a new file for your page called PAGE-NAME.md, replacing PAGE-NAME with a meaningful filename for the page.
4. Add the following YAML frontmatter to the top of the file, replacing PAGE TITLE with the page's title and URL-PATH with a path you want for the page's URL.
      ```
        layout: page
        title: "PAGE TITLE"
        permalink: /URL-PATH/
      ```
5. Below the frontmatter, add content for your page.
6. To specify a page order, you can use the `nav_order` parameter in your pages’ YAML front matter.
      ```
        layout: default
        title: "PAGE TITLE"
        nav_order: 4
      ```

## Customization

### Color schemes

Just the Docs supports two color schemes: light (default), and dark.

To enable a color scheme, set the `color_scheme` parameter in both the `_config.yml` and `_config_local.yml` files.

- Local environment executes the `_config_local.yml` file and github reads the `_config.yml` file

#### Example 
```
# Color scheme supports "light" (default) and "dark"
color_scheme: dark
```

### Custom schemes
You can add custom schemes.
If you want to add a scheme named `foo` (can be any name) just add a file `_sass/color_schemes/foo.scss` (replace `foo` by your scheme name) 
where you override theme variables to change colors, fonts, spacing, etc.

Available variables are listed in the [`_variables.scss`](https://github.com/Commonsense-Run/commonsense-run.github.io/blob/master/_sass/support/_variables.scss) file.

For example, to change the link color from the purple default to blue, include the following inside your scheme file:

#### Example 
```scss
$link-color: $blue-000;
```

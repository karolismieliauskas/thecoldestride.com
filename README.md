### Intro

Site is build using [Jekyll](https://jekyllrb.com). Make sure you've set it up before working with page source. Then run `bundle install` inside source dir.

### Working with site

Mostly you need two commands: `bundle exec jekyll serve` to edit and build site locally. `bundle exec jekyll build` will build your site and output generated static html into `_site/` build folder.

### Tranalsations and copy editing inside the site

i18n translations are powered by [Jekyll multiple languages plugin](https://github.com/Anthony-Gaudino/jekyll-multiple-languages-plugin) plugin. Read it's documentation to understand it's limits and features. For site editors folder `_i18n` is what you are interested in. Each language of the site has it's `.yml` file. Duplicate them if you want to create new site translation and name the file with country shortcode. Then edit `_config.yml` languages section and add new language there.

Edit contents of `en.yml` (or any other language), reload jekyll server or re-run the build to see updates.

### Creating pages

All site structure is visible in `pages/` folder. Duplicate any of the files in there to create new page - make sure it has set unique `namespace` and `permalink`. Add translation keys in translation file (e.g. `_18n/en.yml`). Make sure translation file first key name matches `namespace` in the page's `.html` file. This is you translations keys are linked with page template.

Navigation and links are also editable in translations files. You'll see groups named `links_by_namespace`, this means keys in this group are namespaces of the pages which they are rendering and linking to.



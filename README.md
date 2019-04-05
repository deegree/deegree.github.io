# www.deegree.org 

This Website was created for [Jekyll][1] using the [*Feeling Responsive*][2] Theme from Phlow.


 [1]: https://jekyllrb.com/
 [2]: http://phlow.github.io/feeling-responsive/
 [3]: #
 

## Local Development

A local development environment can be used by installing Ruby (2.6.x) and running the following in the website directory.

```bash
gem install bundler
# inside direcotry containing the Gemfile
bundler install
```

Jekyll can be executed locally with the following command:

```bash
jekyll serve --incremental --config _config.yml,_config_dev.yml
```

**Note:** It can be usefull to clean the `_site` directory before running jekyll to force re-creation of all content (styles etc.).
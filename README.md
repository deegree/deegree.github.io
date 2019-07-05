# www.deegree.org 

This Website was created for [Jekyll][1] using the [*Feeling Responsive*][2] Theme from Phlow.

 [1]: https://jekyllrb.com/
 [2]: http://phlow.github.io/feeling-responsive/
 [3]: #
 
## Local Development

A local development environment can be used by installing Ruby (2.6.x) and running the following in the website directory.

```bash
gem install bundler
# inside directory containing the Gemfile
bundler install
```

Jekyll can be executed locally with the following command:

```bash
jekyll serve --incremental --host=0.0.0.0 --config _config.yml,_config_dev.yml
```

**Note:** It can be useful to clean the `_site` directory before running jekyll to force re-creation of all content (styles etc.).

### Using docker

You can use a docker container with Ruby (2.6.x) to run the web site locally. First pull the image:

```bash
docker pull ruby:2.6.3-stretch
```
On Linux run the container with:
```bash
    docker run -it --rm --name jekyll -v "$PWD":/usr/src/myapp -w /usr/src/myapp -p 4000:4000 ruby:2.6.3-stretch /bin/bash
```

Windows:
```bash
    docker run -it --rm --name jekyll -v "%CD%":/usr/src/myapp -w /usr/src/myapp -p 4000:4000 ruby:2.6.3-stretch /bin/bash
```

Inside the container run the following commands and then continue as described above:

```bash
apt-get update
apt-get install --yes locales
export LC_ALL=C.UTF-8
export LANG=de_DE@UTF-8
```
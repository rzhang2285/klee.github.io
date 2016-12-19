# KLEE Official Website

The KLEE website, built using [Web Starter Kit](http://developers.google.com/web/starter-kit) and [Jekyll](http://jekyllrb.com/).

## Quickstart

You should have a reasonably recent version of Ruby (use [RVM](http://rvm.io/) or [rbenv](https://github.com/sstephenson/rbenv) to get one) and [Bundler](http://bundler.io/) (included in RVM and rbenv, by default). You also have to install Node.js. If you get errors like `Liquid Exception: EPIPE` when you try to run Jekyll, set python 2.x as default (instead of 3.x).

Clone this repository and install all dependencies using:

```bash
$ bundle
```

Then, you can preview the site by running (at `localhost:4000` by default):

```bash
$ bundle exec jekyll serve -w
```

To build the site, you can use:

```bash
$ bundle exec jekyll build
```

## Contributing

Contributions, both to content and design are welcome and encouraged. To contribute, please submit a pull request.

## Adding Release Documentation

The repository has old versions of the documentation in `releases/docs/`. To generate documentation for a release
do the following.

1. Open `_config.yml` and
 - Use `excludes` that excludes the `releases` folder.
 - Change `is_release` to `true`.
 - Set `current_version` to the KLEE version.

2. Run the following command where `<VERSION>` is the KLEE version.

```
$ jekyll build -d releases/docs/<VERSION> --baseurl /releases/docs/<VERSION>
```

3. Clear the changes made to `_config.yml` (e.g. by doing `git reset --hard`).
4. Add `releases/docs/<VERSION>` to the repository.
5. Add an entry for the release in `releases/index.md`.
6. Commit the changes.

## License

Creative Commons Attribution 3.0 Unported (CC BY 3.0)

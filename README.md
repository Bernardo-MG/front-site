# Front Site

My own small personal site, generated with the help of [Jekyll](https://jekyllrb.com). It is just a static site, to showcase my personal projects.

## Usage

### Prerequisites

- Jekyll
- Ruby

### Building

The project can be generated locally:

```
$ jekyll build
```

But as the resource links probably won't work this is only useful for manual deployment

### Local Deployment

To actually test the site it should be published locally:

```
$ bundle exec jekyll serve
```

Now it can be checked at [http://localhost:4000](http://localhost:4000). And it will rebuild the page after any change.

### Remote Deployment

Master is always deployed automatically to the remote server by the CI scripts.

## Collaborate

Any kind of help with the project will be well received, and there are two main ways to give such help:

- Reporting errors and asking for extensions through the issues management
- or forking the repository and extending the project

### Issues Management

Issues are managed at the GitHub [project issues tracker][issues], where any Github user may report bugs or ask for new features.

### Getting the Code

If you wish to fork or modify the code, visit the [GitHub project page][scm], where the latest versions are always kept. Check the 'master' branch for the latest release, and the 'develop' for the current, and stable, development version.

## License

The project has been released under the [MIT License][license].

[issues]: https://github.com/Bernardo-MG/front-site/issues
[license]: http://www.opensource.org/licenses/mit-license.php
[scm]: https://github.com/Bernardo-MG/front-site

# ComposerViz

[![Packagist](https://img.shields.io/packagist/v/sandfoxme/composer-viz.svg?maxAge=2592000)](https://packagist.org/packages/sandfoxme/composer-viz)
[![Packagist](https://img.shields.io/packagist/l/sandfoxme/composer-viz.svg?maxAge=2592000)](https://opensource.org/licenses/MIT)
[![Code Climate](https://img.shields.io/codeclimate/github/sandfoxme/composer-viz.svg?maxAge=2592000)](https://codeclimate.com/github/sandfoxme/composer-viz)

A CLI tool to generate dependency graph by GraphViz inspired by `bundle viz`

## Usage

```
composer-viz [-d|--path PATH] [-o|--output OUTPUT] [-f|--format FORMAT] 
             [--no-dev] [--no-php] [--no-ext] [--no-platform] 
             [--no-pkg-versions] [--no-dep-versions] [--no-versions]
```

`-d|--path PATH`: Set path to the project's `composer.lock` and `composer.json`. If not set, current path will be used  
`-o|--output OUTPUT`: Set output file. If not set, the result will be displayed from temporary file  
`-f|--format FORMAT`: Set output file format. Useful if it is not detected from `--output`  
`--no-dev`: Do not show development dependencies  
`--no-php`: Do not show PHP as a dependency (php and php64)  
`--no-ext`: Do not show extensions as dependencies  
`--no-platform`: `--no-php` + `--no-ext`  
`--no-pkg-versions`: Do not show package versions on graph vertices  
`--no-dep-versions`: Do not show package versions on graph edges  
`--no-versions`: `--no-pkg-versions` + `--no-dep-versions`

## GraphViz

You should install GraphViz on your system first.

Use this in Ubuntu:

````bash
sudo apt-get install graphviz
````

Sometimes you may need additional packages like in Fedora you should also install ``graphviz-gd`` to be able
to export images, like this:

````bash
# dot, svg and postscript work without graphviz-gd but png, jpeg and gif don't
sudo dnf install graphviz graphviz-gd
````

# SpectaQL Dark Theme

A dark theme for SpectaQL based on the default SpectaQL theme.

![dark spectaql theme](./img/screenshot-desktop.png)

In mobile:

<img src="./img/screenshot-mobile.png" width="49%" /> <img src="./img/screenshot-mobile-nav.png" width="49%" />

## Usage

You can use this theme in two ways

1. Pull the theme in as is from npm
2. Fork the repo or otherwise copy the theme

### 1: Using the theme from NPM

The benefit of using the theme directly from NPM is that you will have an easy path to upgrade if/when there are bug fixes and improvements.

Add both `spectaql` and `spectaql-dark-theme` to your repo as dev dependencies:

```sh
$ yarn add -D spectaql spectaql-dark-theme
# OR
$ npm install --dev spectaql spectaql-dark-theme
```

Then you can reference the theme in your SpectaQL config from `node_modules`.

```yaml
spectaql:
  # Use the theme from node_modules
  themeDir: ./node_modules/spectaql-dark-theme/theme
  # The rest of your config...
```

See the [example `config.yml`](https://github.com/anvilco/spectaql/blob/main/examples/config.yml) for a full example.

### 2: Usage by copying

It is likely you will want to modify the theme's colors and override styles. All you need to do is copy the entire [`theme`](/theme) directory into your project. Once you have the `theme` directory in the location of your choice, reference the theme in your SpectaQL config:

```yaml
spectaql:
  themeDir: ./custom-location/docs/theme
```

See the [example `config.yml`](https://github.com/anvilco/spectaql/blob/main/examples/config.yml) for a full example.

## Generating docs with your new theme

When you have your config.yml setup from the one of the usage sections above, you can run SpectaQL as you would otherwise. From the root of your project

```sh
# View docs with a development server
$ yarn spectaql ./spectaql-config.yml -D
# Output docs to a file
$ yarn spectaql ./spectaql-config.yml -t ./build/docs

# View docs with a development server
$ npx spectaql ./spectaql-config.yml -D
# Output docs to a file
$ npx spectaql ./spectaql-config.yml -t ./build/docs
```

## License

MIT

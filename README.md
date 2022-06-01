# SpectaQL Dark Theme

A dark theme for SpectaQL based on the default SpectaQL theme.

![dark spectaql theme](./img/screenshot-desktop.png)

In mobile:

<img src="./img/screenshot-mobile.png" width="49%" /> <img src="./img/screenshot-mobile-nav.png" width="49%" />

---

This theme is provided by [Anvil](https://www.useanvil.com/developers/). Anvil provides easy APIs for all things paperwork.

1. [PDF filling API](https://www.useanvil.com/products/pdf-filling-api/) - fill out a PDF template with a web request and structured JSON data.
2. [PDF generation API](https://www.useanvil.com/products/pdf-generation-api/) - send markdown or HTML and Anvil will render it to a PDF.
3. [Etch e-sign with API](https://www.useanvil.com/products/etch/) - customizable, embeddable, e-signature platform with an API to control the signing process end-to-end.
4. [Anvil Workflows (w/ API)](https://www.useanvil.com/products/workflows/) - Webforms + PDF + e-sign with a powerful no-code builder. Easily collect structured data, generate PDFs, and request signatures.

Learn more on our [Anvil developer page](https://www.useanvil.com/developers/).

## Usage

You can use this theme in two ways

1. Pull the theme in as is from npm
2. Fork the repo or otherwise copy the theme

### 1: Using the theme from NPM

The benefit of using the theme directly from NPM is that you will have an easy path to upgrade if/when there are bug fixes and improvements. See the [example node repo](https://github.com/anvilco/spectaql-theme-example) for an example project using this theme via NPM.

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

## Related materials

* [Building a SpectaQL theme for your GraphQL documentation](https://www.useanvil.com/blog/engineering/building-a-spectaql-theme-for-your-graphql-documentation) - tutorial explaining how to build out a SpectaQL theme similar to this one.

## License

MIT

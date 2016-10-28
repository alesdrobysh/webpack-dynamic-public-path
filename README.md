# Webpack Dynamic Public Path Plugin

The purpose of this plugin is to assign to webpack public path a value that isn't known at build time.

It is extremely helpful when you prepare a build for Salesforce Visualforce page because in this case developer don't know path to static resource until it is downloaded to SLDC.

## Usage

Installation is easy with npm:

    npm install webpack-dynamic-public-path-plugin

Then require it in your webpack config and add it to a plugins section:

```javascript
plugins: [
    new DynamicPublicPathPlugin({
        publicPath: 'window.publicPath + "/"',
        outputPath: 'bundle'
    })
]
```

where `publicPath` option stores expression that will evaluate to actual public path in runtime and `outputPath` is a folder where your bundle is saved to.


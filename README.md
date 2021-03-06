A JSDoc plugin that transforms ES6 source files with Babel before they are processsed.

## Installation

The `jsdoc-babel` plugin can be installed using NPM.

```bash
npm install jsdoc-babel --save-dev
```

## Usage

To use plugin you should include the plugin module in the `plugins` array of [JSDoc's configuration file](http://usejsdoc.org/about-configuring-jsdoc.html).

```json
{
    "plugins": ["node_modules/jsdoc-babel"]
}
```

### Processing files with different extensions

By default, the plugin only processes files that have a `.js` extension. You could enable transformation for other file extensions by adding the following settings to your JSDoc configuration file:

```json
{
    "plugins": ["node_modules/jsdoc-babel"],
    "babel": {
        "extensions": ["js", "es6", "jsx"]
    }
}
```

### Passing options through Babel

You can define [options](http://babeljs.io/docs/usage/options/) to be passed through Babel by adding them to your JSDoc configuration file:

```json
{
    "plugins": ["node_modules/jsdoc-babel"],
    "babel": {
        "optional": ["runtime"]
    }
}
```

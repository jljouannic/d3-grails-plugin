D3.js Grails plugin
===

D3.js (Data-Driven Documents) is a JavaScript library for manipulating data and bring it to life using HTML, SVG and CSS.

This plugin simply provides a resource file for d3.js.

Installation
---

Edit `BuildConfig.groovy` and add the following plugin dependency:

```Groovy
runtime ":d3:3.4.8.0"
```

###Version number

The version number of this plugin follows the version number of the D3.js version it bundles, with possible 4th-level
point releases for patches/iterations of the plugin with the same D3.js library.

For example, the first release of this plugin is 3.4.8.0 because it provides D3.js 3.4.6. If there was a problem with
this release, this might change to 3.4.8.1, 3.4.8.2, etc.

Usage
---

This plugin supports both the [Resources Plugin](http://grails.org/plugin/resources) and the
[Asset Pipeline Plugin](http://grails.org/plugin/asset-pipeline)


### Resources Plugin

This plugin provides a `D3Resources.groovy` file in which a `d3` module is defined.
So, adding a reference to the D3.js library can be done by adding the following in GSP page header:

```html
<r:require modules="d3"/>
```

### Asset Pipeline Plugin

To use Asset-Pipeline to add a dependency to D3.js in your JavaScript code, you just have to write a `require` directive
at the beginning of you JavaScript file:

```JavaScript
//= require d3
console.log("And here begins my code");
```

---

See [D3.js web site](http://d3js.org/) for documentation and many great examples to get you started.


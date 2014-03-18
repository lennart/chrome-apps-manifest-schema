# chrome-apps-manifest-schema

JSON Schema for validating Chrome Apps manifest.json

This module provides a [JSON Schema](http://json-schema.org) (v4) that
describes Chrome Apps manifest.json files. To validate a JSON file against
the schema, you will need to use a [JSON Schema
validator](http://json-schema.org/implementations.html#validator-list) with v4
support.


Example using the [TV4 validator](http://geraintluff.github.io/tv4/) via the
[grunt-tv4 plugin](https://github.com/Bartvds/grunt-tv4) to validate a
"manifest.json" file:

```coffeescript
# Gruntfile.coffee

module.exports = (grunt) ->
  grunt.initConfig
    tv4:
      manifest:
        src: "manifest.json"
        options:
          root: require('chrome-apps-manifest-schema')

  grunt.loadNpmTasks "grunt-tv4"
  grunt.registerTask 'default', 'tv4'
```

## Credits

Built upon [chrome-extension-manifest-schema](https://github.com/jasonkarns/chrome-extension-manifest-schema) for [tv4](https://github.com/geraintluff/tv4) this schema will _try to_ validate your manifest.json against the current chrome apps manifest [taken from the official chrome apps documentation by google](https://developer.chrome.com/apps/manifest). If this link breaks, or the schema implemented here differs from the authoritative source, please tell me so.

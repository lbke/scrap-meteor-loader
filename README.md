# Scrap Meteor Loader

A Webpack loader for Meteor packages, that drops Meteor packages.

**/!\ This package is still experimental, use with caution. **

This package will agressively scrap out `meteor/` imports from files. This allows to load Meteor packages using Webpack. Of course, the associated imports will become undefined, so errors may appear at runtime.

We use this scraper in [Vulcan.js](http://vulcanjs.org/) to be able to run components in Storybook. The Meteor packages and variables we actually needs are either mocked, or replaced using another specific loader [vulcan-loader](https://github.com/lbke/vulcan-loader)

## Loader options

- `preserve`: Meteor packages ignored by the loader. Use to mock some necessary packages or to load them with another method.
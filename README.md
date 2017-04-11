# Binary Ninja Community Plugins

Repository to track Binary Ninja Community Plugins, Themes, and other related tools

## Plugins

Plugins in this repository are provided by the community. Vector 35 LLC makes no guarantees to the quality, safety or efficacy of the plugins herein.

### Installing Plugins

To install plugins, you can either clone this repository, or clone the specific plugin you are interested in into your [plugin folder](https://github.com/Vector35/binaryninja-api/tree/dev/python/examples#loading-plugins).

### Contributing Plugins

 1. Create a new repository (Optionally, just copy it from the [sample plugin](/Vector35/official-plugins/official/sample_plugin/))
 1. Fill out a [`plugin.json`](/Vector35/official-plugins/plugins/sample_plugin/plugin.json)
 1. (Optional) Run `generate-readme.md` to update your readme and license 
 1. File an [issue]((/Vector35/community-plugins/issue) with a link to your repo, or issue a [pull request](/Vector35/community-plugins/pull/new/master)
 
#### Required Fields

To be displayed in the plugin loader, your `plugin.json` MUST have the following fields:

 - `name`
 - `author`
 - `api`
 - `license['name']`
 - `description`
 - `version`
 
All other fields are optional.

## License

Note that content contained in the root of this repository itself is Copyright 2016, Vector 35 LLC and [available](LICENSE) under an MIT license, but each individual plugin may be released under a different license.
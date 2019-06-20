# Binary Ninja Community Plugins

Plugins in this repository are provided by the community. Vector 35 LLC makes no guarantees to the quality, safety or efficacy of the plugins herein.

## Installing Plugins

To install plugins, you can either use the Plugin Manager in the UI or clone the repositories linked here in into your [plugin folder](https://github.com/Vector35/binaryninja-api/tree/dev/python/examples#loading-plugins).

## Contributing Plugins

 1. Create a new repository (Optionally, just copy it from the [sample plugin](https://github.com/Vector35/sample_plugin))
 1. Fill out a [`plugin.json`](https://github.com/Vector35/sample_plugin/blob/master/plugin.json). Optionally you can use the `generate_plugininfo.py -i` to interactively walk you through setting the required fields. The `plugin.json` must pass all the checks when run through `generate_plugininfo.py -v plugin.json`. `generate_plugininfo.py` can also generate your `README.md` and your `LICENSE` file with the `-r`, `-l`, or `-a` (all) options. Below is a list of the required and recommended fields.
 1. Create and push a git tag with the version of your plugin (e.g. `v1.1`). Create a release, optionally attaching build artifacts as required.
 1. File an [issue](https://github.com/Vector35/community-plugins/issues) with a link to your repo and the tag name of the release.
 1. To update your plugin repeat the two previous steps.

### Required Fields

To be displayed in the plugin loader, your `plugin.json` MUST have the following fields:

 - `pluginmetadataversion` - The current version is the integer `2`
 - `name` - Good names do not use "Binary Ninja" or "Binja" neither do they use the words "plugin" or "extension". So instead of "Binja 6502 Architecture Plugin" simply use "6502 Architecture"
 - `author` - Your name, handle, or company name.
 - `api` - A list of supported architectures. Though we support `python2` and `python3` we highly recommend plugin authors support `python3` as `python2` support will be dropped as some time in the near future.
 - `license` - A json object with `name` and `text` keys.
 - `description` - This is a short (<50 character) description of the plugin.
 - `longdescription` - A longer Markdown formatted description of the plugin including hyperlinks and images as needed.
 - `version` - Version string
 - `minimumBinaryNinjaVersion` - An integer _build number_ so instead of `1.1.555` use `555`.
 - `platforms` - A list of strings one for each supported platform. Valid platforms are `Darwin`, `Linux`, and `Windows`

### Recommended Fields

 - `type` - A list of strings of the following types: `core`, `ui`, `architecture`, `binaryview`, and `helper`.
   - `helper` - Plugin that adds some base functionality to Binary Ninja. Most plugins will be of this type.
   - `ui` - The plugin extends the UI is some way.
   - `architecture` - The plugin adds an architecture (e.g. `x86`, `ARM`, `MIPS`).
   - `binaryview` - The plugin adds a new BinaryView (e.g. `PE`, `MachO`, `ELF`).
   - `core` - Plugin that extends the core's analysis. Your plugin probably isn't one of these.
 - `installinstructions` - A json object with keys for each supported platform listed in `platforms` and text Markdown formatted.

## License

Note that content contained in the root of this repository itself is Copyright 2016, Vector 35 LLC and [available](LICENSE) under an MIT license, but each individual plugin may be released under a different license.

# Binary Ninja Plugins

| PluginName | Author | Last Updated | License | Type | Description |
|------------|--------|--------------|---------|----------|-------------|
|[Bookmarks](https://github.com/joshwatson/binaryninja-bookmarks)|[Josh Watson](https://github.com/joshwatson)|2016-10-11|MIT|core, ui|A plugin that adds bookmarking functionality.|
|[MSP430 Architecture Plugin](https://github.com/joshwatson/binaryninja-msp430)|[Josh Watson](https://github.com/joshwatson)|2016-10-10|MIT|architecture, core, ui|A disassembler and lifter for the MSP430 architecture.|
|[SigMaker](https://github.com/Alex3434/Binja-SigMaker)|[Alex3434](https://github.com/Alex3434)|2018-09-26|MIT|architecture, binaryview, core, ui|Generate Signatures|

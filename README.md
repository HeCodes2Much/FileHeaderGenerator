# File Header Generator

The File Header Generator extension aims to quickly generate readable headers for several programming languages. Additionally, it also automatically updates the last edited time.

## Features

The File Header Generator generates headers in one, pre-determined lay-out. This layout displays a more readable type of file name, the creator of the file, when the file was created and when the file was edited most recently. Additionally, it also shows a description (see the picture below for an example).

![Example Header](images/header_example.png)  
_Image using the [Dracula Syntax](https://marketplace.visualstudio.com/items?itemName=dracula-theme.theme-dracula) theme_

The creation of a new header is really easy. Simply run the command: "Generate Header" from the command palette, type a discription for your file and hit enter. This description can, of course, also be added later on by editing the header manually. Note that when adding the header via the input box, it is automatically hard-wrapped to a total of 79 characters per line.

When the header is generated, it is automatically maintained (i.e., the 'Last Edited' date is updated) every time the file is saved. To stop this behaviour, set 'Auto updated?' to no or remove it altogether.

## Supported Languages

- python
- shellscript
- perl
- fish
- lua
- coffeescript

For the full list that this plugin supports check [Language Support](LANG_SUPPORT.md)

## Commands

The File Header Generator extension current contributes the following command:

- `file-header-generator.generateHeader`: Generates a header in the current file. Once run, it first prompts the user to input a description, which will automatically be linewrapped in the resulting header. The header will be placed at the start of the file, before any text already present.

## Extension Settings

This extension contributes the following settings:

- `file-header-generator.enabled`: Enables or disables this extension.
- `file-header-generator.username`: Set your own name to sign the headers generated with this extension.
- `file-header-generator.searchLines`: Number of lines to search for the Auto Updated and Last Edited fields. More lines means more extensive search on non-updated files, but more lines allows for more complicated headers before the fields can appear.
- `file-header-generator.dateFormat`: The format of dates written by the FileHeaderGenerator. Is set to the current locale by default (see the list of special tokens below). For an overview of the tokens available, refer to [https://moment.github.io/luxon/#/formatting?id=table-of-tokens](https://moment.github.io/luxon/#/formatting?id=table-of-tokens.). Additionally, there are a few extra values:
  - `<locale>`: Formats according to the standard locale, as reported by the system. Can also use the `FFF` format for this.
  - `<iso>`: Formats according to the standard ISO format.

## Issues

If you encounter any issues, have suggestions or would like something to change, don't hesitate to leave an issue at our [github](https://github.com/The-Repo-Club/FileHeaderGenerator/issues)! Please try to use the appropriate tags so I can process them more efficiently.

Also note that I'm mostly making this extension for myself - that means that I might not respond to issues immediately or incorporate them, even if they're super good ideas.

## Release Notes

See the release notes for each version below. For a full overview, check [CHANGELOG.md](CHANGELOG.md).

## [1.0.3] - 20-01-2022

- Fixed She-Bang
- Added more languages
- Added Dependencies

### [1.0.2] - 19-01-2022

- Added Github

### [1.0.1] - 19-01-2022

- Added She-Bang

### [1.0.0] - 19-01-2022

- Initial release of the extension.

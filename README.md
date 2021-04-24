# `emojitools`
_the cool slack emoji manipulation interface for cool kids_

### Usage

First, install the package into your project.

```
npm install @slwulf/emojitools
```

Then, import the package and execute a command.

```js
const Emojitools = require('@slwulf/emojitools')
const cli = 'effects +Intensify http://path.to/my/image'

Emojitools.fromCommandLineInput(cli)
    .then(image => image.writeToFile())
    .then(filepath => console.log(filepath))
```

Emojitools is intended to be used as a command line or chat bot interface, so its primary surface is the method `EmojiTools.fromCommandLineInput`, which receives raw user input.

The package exposes an image interface as its execution result that allows you to access or further modify a command's output. Read below for more details on working with the image output.

The command line interface has built-in help text for each command. Entering `emojitools --help` will expose a list of commands, and `emojitools <command> --help` describes each command and its inputs.

### API Documentation

- **`Emojitools.fromCommandLineInput(cli[, opts])`**
    - `cli` _\(string\)_ the command line input
    - `opts` _\(object\)_ render and behavior options
    - Returns a Promise that resolves to an [`Image`](models/image.js) instance.

TODO document error handling
TODO add an option for slackdown vs text-only help text
    - pass the param into the help method and let commands decide what to return

### Working with image output

TODO document the Image class

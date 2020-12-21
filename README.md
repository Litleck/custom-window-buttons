# No Linux Frame

No Linux Frame is a plugin for the Discord modification known as Powercord. What this plugin will do is add minimize, maximize, and close buttons to the toolbar, along with making it draggable.

## Note
This plugin was designed only for Linux distributions, not for Windows or any other operating system.

It is very likely with the eventual release of V3 for Powercord that this plugin will no longer work.

## Installation
Due to Powercord limitations installation isn't as simple as other plugins. 

To install this plugin clone it with the command below.


```bash
git clone https://github.com/Litleck/no-linux-frame.git
```

For the plugin to look proper you will need to edit a file that is a part of Powercord. This file can be found in your powercord install directory at `/src/browserWindow.js`

Open `browserWindow.js` in your preferred editor and look for:

```js
if (transparency) {
  opts.transparent = true;
  opts.frame = process.platform === 'win32' ? false : opts.frame;
  delete opts.backgroundColor;
}
```

Right below this segment of code add the following:

```js
opts.frame = false;
```

Save the file then fully restart your Discord client. If all is done correctly the frame should be gone there should be minimize, maximize and close buttons on the toolbar.

## Contributing
Pull requests are welcome. For any bugs, please open an issue first so we can discuss.

## License
[MIT](https://choosealicense.com/licenses/mit/)

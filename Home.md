#### Getting Started
Scratch Blocks is based on Google's [Blockly](https://developers.google.com/blockly) project. For a full API reference please see Google's [Custom Blocks](https://developers.google.com/blockly/custom-blocks/overview) documentation.

#### Installation


#### Building
Before sharing with users, we recommend that you build and compress Scratch Blocks. Building requires [Python 2](https://www.python.org/downloads/) and an internet connection as it uses Google's online [Closure Compiler](https://developers.google.com/closure/compiler/). Once you are ready, you can build by running the following in your console:

```bash
python build.py
```

This will export multiple files including:
```
blockly_uncompressed_vertical.js
blockly_uncompressed_horizontal.js
blockly_compressed_vertical.js
blockly_compressed_horizontal.js
blocks_compressed.js
msg/js/en.js
```

These can then be used in your project by updating the HTML of your application:
```html
<script src="blockly_compressed_horizontal.js"></script>
<script src="blocks_compressed.js"></script>
<script src="msg/js/en.js"></script>
```
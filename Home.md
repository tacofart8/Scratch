#### Getting Started
Scratch Blocks is designed to easily install into any web application. The blocks are 100% client-side, requiring no support from the server. There are no 3rd party dependencies and everything is open source.

Scratch Blocks is based on Google's [Blockly](https://developers.google.com/blockly) project. For a full API reference please see Google's [Custom Blocks](https://developers.google.com/blockly/custom-blocks/overview) documentation.

#### Installation
First, download the source code from GitHub. As this project is quickly being updated we recommend you use [git](https://git-scm.org) but you are more than welcome to [download the code](https://github.com/LLK/scratch-blocks/archive/develop.zip) directly as well.

Once you have the code, point your browser at `tests/horizontal_playground.html` and verify that blocks can be dragged around. In addition to being the "hello world" test for Scratch Blocks, the playgrounds are also useful for testing more advanced features including event handling, right-to-left (RTL), and stack highlighting.

#### Configuration
Configuration of the workspace is *mostly* the same between Blockly and Scratch Blocks but is subject to change as the project continues to develop. Below is a list of configuration options that we are likely to continue to support:

<table>
    <tr>
        <td>Name</td>
        <td>Type</td>
        <td>Description</td>
    <tr>
    <tr>
        <td><code>horizontalLayout</code></td>
        <td><code>boolean</code></td>
        <td>If true, uses the horizontal grammar for displaying blocks. Defaults to false.</td>
    <tr>
    <tr>
        <td><code>rtl</code></td>
        <td><code>boolean</code></td>
        <td>If true, mirror the editor (for Arabic or Hebrew locales). Defaults to false.</td>
    <tr>
    <tr>
        <td><code>media</code></td>
        <td><code>string</code></td>
        <td>Path from page (or frame) to the Scratch Blocks media directory.</td>
    <tr>
    <tr>
        <td><code>scrollbars</code></td>
        <td><code>boolean</code></td>
        <td>Sets whether the workspace is scrollable or not. Defaults to true if the toolbox has categories, false otherwise.</td>
    <tr>
    <tr>
        <td><code>sounds</code></td>
        <td><code>boolean</code></td>
        <td>If false, don't play sounds (e.g. click and delete). Defaults to true.</td>
    <tr>
    <tr>
        <td><code>zoom</code></td>
        <td><code>object</code></td>
        <td>Configures zooming behavior. See <a href="https://developers.google.com/blockly/installation/zoom">zoom API details</a>.</td>
    <tr>
</table>

---

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
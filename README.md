# Jsonnet Support for Visual Studio Code

This extension provides the following helper tools for writing 
[Jsonnet][jsonnet] files in Visual Studio Code. These files 
can be defined with the `.jsonnet` or `.libsonnet` file extension.

* Syntax highlighting
* Markdown-style preview pane for YAML or JSON output
* Tooltip help for [writing **ksonnet** files][ksonnet] 
for Kubernetes configurations

![Jsonnet preview][jsonnet-demo]

## Install

For syntax highlighting only, follow the instructions at 
https://marketplace.visualstudio.com/items?itemName=heptio.jsonnet.

The Jsonnet preview pane requires the Jsonnet command line tool.
Run:

```bash
brew install jsonnet
```

Add the path to the Jsonnet executable to your $PATH. Or you 
can specify it in the `jsonnet.executablePath` field of your 
VS Code `settings.json`.

NOTE: On Windows, you must specify `jsonnet.executablePath`.

## Configure and run

Syntax highlighting requires no additional setup.

To view the preview pae, you can use the default keyboard shortcuts:

* On Mac OS: Shift-Command-I
* On Windows: Ctrl+Shift+I

Or you can customize these shortcuts in the VS Code `keybindings.json` file.

You can also specify the following VS Code settings:

* `jsonnet.extStrs`: An object that defines a set of key-value pairs. 
Lets you customize external variables to pass to the `jsonnet` command line. 
For example, you can set different variables for different projects in a 
workspace configuration. Default value null.
* `jsonnet.outputFormat`: lets you specify whether to preview the output
in JSON or YAML. Default value `yaml`.
* `jsonnet.server`: lets you specify a Jsonnet language server for static
analysis. Default value null.

[jsonnet]: http://jsonnet.org/ "Jsonnet"
[ksonnet]: https://github.com/ksonnet/ksonnet-lib "ksonnet"
[jsonnet-demo]: https://raw.githubusercontent.com/heptio/vscode-jsonnet/master/images/kube-demo.gif

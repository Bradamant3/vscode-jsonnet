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

## Configure and run

Syntax highlighting requires no additional setup.

To view the preview pane, you can use the default keyboard shortcut:

* On Mac OS: Shift-Command-I

Or you can customize the following settings in the VS Code `keybindings.json` file:

* `jsonnet.preview`: keybinding to view the Jsonnet preview in a separate tab from your code. No default keybinding.
* `jsonnet.previewToSide`: keybinding to view the Jsonnet preview in a separate pane, side-by-side with your code. Default is Shift-Command-I.

You can specify the following VS Code settings in your `settings.json` file:

* `jsonnet.executablePath`: Path to the Jsonnet executable. Default value null. You can specify this path here, or in your $PATH environment variable instead.
* `jsonnet.extStrs`: An object that defines a set of key-value pairs. Lets you customize external variables to pass to the `jsonnet` command line. For example, you can set different variables for different projects in a workspace configuration. Default value null.
* `jsonnet.libPaths`: lets you specify additional paths to search for libraries when compiling Jsonnet code. Default value null.
* `jsonnet.outputFormat`: lets you specify whether to preview the output in JSON or YAML. Default value `yaml`.

[jsonnet]: http://jsonnet.org/ "Jsonnet"
[ksonnet]: https://github.com/ksonnet/ksonnet-lib "ksonnet"
[jsonnet-demo]: https://raw.githubusercontent.com/heptio/vscode-jsonnet/master/images/kube-demo.gif

# ImJoy Project Template

This is a template for project layout we propose for projects supporting ImJoy plugins. The overall organization is standard and your code can very well be use without ImJoy. 


[Click here](https://imjoy.io/#/app?repo=imjoy-team/imjoy-project-template) to use this repo in ImJoy.


Additonal information for the files:

1. File **`manifest.imjoy.json`**: specifies how your ImJoy plugins will be shown in the ImJoy plugin import menu

1. Folder **`src`**: your ImJoy plugin files along with other related source code.

1. File **`src/update_manifest.js`** a script for updating the plugin manifest file `manifest.imjoy.json`, this generated file will be read by ImJoy.


## After adding a new plugin

You can place your imjoy plugin file (`*.imjoy.html`) in any folder organization, once added, please run `node src/update_manifest.js` to update the plugin list.

Note: in order to run the command, you need to install [nodejs](https://nodejs.org/).

You can also setup a CI (e.g. Github Actions) to do this for every new commit.


## Creating url to automatically install your plugins
The ImJoy plugin files can be used to [generate a url](http://imjoy.io/docs/index.html#/development?id=distributing-your-plugin-with-url) which automatically opens ImJoy and installs your plugin with all dependencies. 

This example install the template plugin: [Template Plugin](https://imjoy.io/#/app?plugin=https://raw.githubusercontent.com/oeway/ImJoy-project-template/master/imjoy-plugins/templatePlugin.imjoy.html)

Once the plugin is installed, click `Template Plugin` in the plugin menu and follow the instructions in the dialog to install the Python Plugin Engine. You can then execute the plugin. 

### Using tags
ImJoy plugins can have different **[tags](http://imjoy.io/docs/index.html#/development?id=plugins-and-tags)** determining how the plugin is shown in the interface and how it is executed, e.g. to allow processing either on a CPU or GPU. These tags can be set in the url, and you can provide different options to the user.  






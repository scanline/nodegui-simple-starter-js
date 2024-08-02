nodegui-simple-starter-js
=========================
A [NodeGui](https://docs.nodegui.org/) application starter aiming to be fast and simple so that you can take it as a starting point and expand it to meet your needs.
It is a modification of [nodegui-simple-starter](https://github.com/sedwards2009/nodegui-simple-starter) by Simon Edwards, to use Javascript instead of Typescript.

The application itself is a very simple example which opens a window with some text and buttons in it. It also shows how to reference files elsewhere in the project.

This project can work with either `npm` or `yarn`.

Installation
------------

`git clone https://github.com/scanline/nodegui-simple-starter-js`

Set up
------
Run `npm install` to download and install the dependencies.

Building
--------
`npm run build` will take the Javascript code in `src` and produce a bundle file in `dist`.


Running
-------
`npm run run` will run the bundled application. Note, you will have to build it first.


Packaging
---------
`npm run package` will run [Jam Pack NodeGui](https://github.com/sedwards2009/jam-pack-nodegui) with a configuration file to create the relevant packages for the current operating system this is running on. The output appears in `tmp-jam-pack-nodegui/jam-pack-nodegui-work/`.


Configured Scripts
------------------

* `build` - Builds in production mode.
* `start` - Builds in debug mode and runs the application.
* `clean` - Deletes the temporary files.
* `run` - Runs the application from the `dist` folder.
* `package` - Build packages for the application. The output appears in `tmp-jam-pack-nodegui/jam-pack-nodegui-work/`


Making it Yours
---------------
If you decide to use this a starting point for your own project, you will need to first update a number of configuration files which hold details of your project.

* `package.json` - The usual `name`, `description`, `author`, `license`, `repository url`, and `keywords` fields will need to be updated.
* `packaging/jam-pack-nodegui.json` - Many of the configurations for the different package types contain meta-data and package details which need updating. Also, icons will need to be replaced.
* `README.md` - This readme file will also need some heavy editing.

Troubles
--------

After installing and trying to run the application using `npm start` on windows, you might encounter a message like:
```
webpack 5.93.0 compiled successfully in 120 ms
node:internal/modules/cjs/loader:1243
  return process.dlopen(module, path.toNamespacedPath(filename));
                 ^
Error: The specified module could not be found.
```

Though it's obviously not obvious, this message is thrown if you don't have the Visual C++ 2019 Redistributables installed on your system.

Go get 'em here: [VC_redist.x86](https://aka.ms/vs/16/release/VC_redist.x86.exe) - [VC_redist.x64](https://aka.ms/vs/16/release/VC_redist.x64.exe)
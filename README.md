## Develop a nativescript-angular plugin now

[![Angular 2 Style Guide](https://mgechev.github.io/angular2-style-guide/images/badge.svg)](https://github.com/mgechev/angular2-style-guide)
[![MIT license](http://img.shields.io/badge/license-MIT-brightgreen.svg)](http://opensource.org/licenses/MIT)
[![Dependency Status](https://david-dm.org/NathanWalker/nativescript-ng2-plugin-seed/status.svg)](https://david-dm.org/NathanWalker/nativescript-ng2-plugin-seed#info=dependencies)

| ![Demo](/resources/demo.png) |
| :---: |
| Android and iPhone running the same {N} + Angular2 plugin. |

The seed is setup to allow you to create a [nativescript-angular](https://github.com/NativeScript/nativescript-angular) plugin quickly.

* Sample demo app ready for you to try out your plugin as you develop it.
* Sample `Component`, `Directive`, `Pipe` and `Service` created for you (*tests coming soon*) to get started right away.
* Customize whichever is helpful to your plugin and remove the others.

## Get started

1. Download a zip of this seed.
2. `cd ... path/to/unzip/folder ...`
3. `npm install -g typescript`
4. `npm install -g nativescript`
5. `npm install`
6. `npm run setup`
7. Get to work.

## Changes needed

You will want to change a couple things for your plugin.

1. Replace all instances of `nativescript-ng2-yourplugin` with name of *your* plugin:
  * Here: https://github.com/NathanWalker/nativescript-ng2-plugin-seed/blob/master/package.json
  * Here: https://github.com/NathanWalker/nativescript-ng2-plugin-seed/blob/master/src/package.json#L16
  * Here: https://github.com/NathanWalker/nativescript-ng2-plugin-seed/blob/master/tsconfig.json#L14 (And likely modify more to tailor to your specific plugins typescript definition needs)
2. Modify the demo to import your plugin files, etc: https://github.com/NathanWalker/nativescript-ng2-plugin-seed/blob/master/src/app/app.ts#L10-L15

## Develop Workflow

Make changes to plugin files, then:

```
npm run demo.ios

// or...

npm run demo.android
```

### Build Plugin

You'll want to run this before publishing.

```
npm run build
```

**VERY IMPORTANT**: You need to modify `package.json` for your plugin. Most likely, you will want to remove 3 sections completely: `scripts`, `dependencies`, and `devDependencies` as those are setup for the demo. When publishing, it's important to ensure no unnecessary scripts or dependencies are installed when comsumers use your plugin. You can add those sections back *after* publishing.

### Testing

Work in progress. Coming soon.

```
npm test
```
### Troubleshooting

When preparing your demo if you get the following error message:

```
Plugin "nativescript-ng2-yourplugin" is not installed.
Sending exception report (press Ctrl+C to stop).....
```
This means your plugin has not been copied over to the demo project, or failed when running the demo command previously. To resolve this run ``npm run repair``.

## Why the TNS prefixed name?

`TNS` stands for **T**elerik **N**ative**S**cript

iOS uses classes prefixed with `NS` (stemming from the [NeXTSTEP](https://en.wikipedia.org/wiki/NeXTSTEP) days of old):
https://developer.apple.com/library/mac/documentation/Cocoa/Reference/Foundation/Classes/NSString_Class/

To avoid confusion with iOS native classes, `TNS` is used instead.

# License

[MIT](/LICENSE)

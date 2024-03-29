# NOTICE

## Want something even better? Use the new version [bombino](https://github.com/Inventsable/bombino) instead.

---

## Generate an Adobe CEP extension in a few simple steps:

![](https://thumbs.gfycat.com/GloriousAlarmingInchworm-size_restricted.gif)

---

## Contributors

Special thanks to Adam and Eric for their invaluable (and shockingly free) help

| <a href="https://github.com/Inventsable"><img src="https://avatars2.githubusercontent.com/u/37279677?s=460&v=4" alt="tom" width="100"/></a> | <a href="https://github.com/adamplouff"><img src="https://avatars1.githubusercontent.com/u/8580225?s=460&v=4" alt="adam" width="100"/></a> | <a href="https://github.com/ericdrobinson"><img src="https://avatars0.githubusercontent.com/u/9142587?s=460&v=4" alt="eric" width="100"/></a> |
| :-----------------------------------------------------------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------------------------: |
|                                              [Tom Scharstein](https://github.com/Inventsable)                                               |                                                [Adam Plouff](https://github.com/adamplouff)                                                |                                               [Eric Robinson](https://github.com/ericdrobinson)                                               |
|                                                                   Creator                                                                   |                                                              General Wizardry                                                              |                                                               Inspector General                                                               |

---

## Installation

First, install [Yeoman](http://yeoman.io) and generator-quasar-vue-cli using [npm](https://www.npmjs.com/) (we assume you have pre-installed [node.js](https://nodejs.org/)).

```bash
npm install -g yo
npm install -g generator-cep-quasar-cli
```

Then generate your new project:

```bash
# Recommended inside ../AppData/Roaming/CEP/extensions
yo cep-quasar-cli

# Prompt for name
# Prompt for template
# Prompt for Adobe apps to be included in manifest and typescript
# Prompt for base localhost port
```

## Templates

See more information about usage:

- [Plus](https://github.com/Inventsable/cep-quasar-cli-plus) (Quasar, Router, Lottie, Vuex, external Modal Dialogs)

---

## Commands

Each template comes with 5 commands baked in ([see details here](https://github.com/Inventsable/CEP-Self-Signing-Panel#what-do-they-do)):

- `npm run help` - A full list of the commands available and descriptions.
- `npm run switch` - Reports whether in developer or production context and can switch automatically.
- `npm run update` - Reports current version of panel in manifest and prompts to update Major, Minor, or Micro.
- `npm run register` - Reports the current user data (if any) and prompts to save new info to be used in certificates.
- `npm run sign` - Automatically stages and signs the extension, placing it in a `./archive` directory within the current panel.

---

## Extras and Add-ons

- [starlette](https://github.com/Inventsable/starlette) _(Shipped in all templates)_ - Color and theming engine that handles all host app colors and exposes them as reactive CSS variables to save you the need to do any theme or color logic yourself.
- [leylo](https://github.com/Inventsable/leylo) - Library to integrate a Firebase backend into any panel with a single command and line of code, providing over 40 CRUD actions for Firestore database.
- ~~[FS Example](https://github.com/Inventsable/CEP-FS-Example) - Demonstration of how to include `require()` for both Dev and Production contexts (needed due to being mixed content within an iframe while in Developer context)~~ **No longer needed!** Panels now automatically work with `require()` with no additional steps regardless of context.

## License

MIT © [Tom Scharstein](www.inventsable.cc)

---

# TODO

- Drop Yeoman. Why is this a generator? It doesn't use any Yeoman commands but carries all the security vulnerabilities.
- Consolidate both generators into a new NPM package, which asks what build system (Vue/Quasar) to use then continues

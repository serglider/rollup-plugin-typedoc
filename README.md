<!-- ![npm](https://img.shields.io/npm/v/shake-detector)
![npm bundle size](https://img.shields.io/bundlephobia/minzip/shake-detector)
![NPM](https://img.shields.io/npm/l/shake-detector)
![GitHub top language](https://img.shields.io/github/languages/top/serglider/shake-detector) -->

<!--- https://shields.io/ badges -->

# rollup-plugin-typedoc
This plugin runs [Typedoc](https://typedoc.org/) to generate your API documentation as a step of your [Rollup](http://rollupjs.org/) flow.

## Setup

```bash
npm i rollup-plugin-typedoc --save-dev
```

Typedoc is required as peer dependency. 
```bash
npm i typedoc --save-dev
```
<!-- todo: no-.nojekyll -->
## Usage
```js
import typescript from '@rollup/plugin-typescript';
import typedoc from 'rollup-plugin-typedoc';

// see https://typedoc.org/guides/options/
const options = {
    out: './docsDir',
    entryPoints: ['./src'],
};
// the plugin reads tsconfig.json, typedoc.json,
// and your custom options (as above) and merges them
export default [
    {
        input: 'src/index.ts',
        plugins: [
            typescript(),
            typedoc(options)
        ],
    }
];
```
__Note:__ do not include this plugin for your watch configurations for performance reasons.

## License

Copyright © 2021, [Sergey Chernykh](https://github.com/serglider).
Released under the [MIT License](LICENSE).

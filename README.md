extended-emitter-es6
====================

A port of [extended-emitter](https://github.com/khrome/extended-emitter) to an external module so I can make something mocha testable in node without recompilation. It uses any library shimmed against a `Emitter` object, which allows you to shim in whatever you need via that global or other means (subprocess, sandbox, etc).

At some point in the future this code will be reunified (as soon as import, require, AMD, commonjs and browser globals can all be accomodated in a single file without transpile).

Compatible with native browser imports, native node imports and towers of babel. For example in the browser, assuming you are serving statically out of root on port `8000`, use the following mapping:

```json
{
    "sift": "http://localhost:8000/node_modules/extended-emitter-es6/node_modules/sift/es5m/index.js",
    "extended-emitter-es6": "http://localhost:8000/node_modules/extended-emitter-es6/extended-emitter-es6.js",
}
```

and it will load without any kind of compile process (while remaining compatible with one).


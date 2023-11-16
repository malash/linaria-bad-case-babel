# Bad case demo for Linaria babel preset

## How to run

```bash
yarn
yarn start
```

## Bad case

You should checkout the `master` branch. The folder structure looks like this:

```
├── package.json
├── src
│   └── index.ts
└── yarn.lock
```

The `src/index.ts` file contains only one line: `const a: number = 1;`.

The `yarn start` command will run `babel --presets=@babel/typescript,@linaria src/index.ts` and output will be:

```
yarn run v1.22.19
$ babel --presets=@babel/typescript,@linaria src/index.ts
SyntaxError: /Users/malash/Projects/test-goji/src/index.ts: /Users/malash/Projects/test-goji/src/index.ts: Missing initializer in const declaration. (1:7)

> 1 | const a: number = 1;
    |        ^
  2 |
    at constructor (/Users/malash/Projects/test-goji/node_modules/@babel/parser/lib/index.js:356:19)
    at Parser.raise (/Users/malash/Projects/test-goji/node_modules/@babel/parser/lib/index.js:3223:19)
    at Parser.parseVar (/Users/malash/Projects/test-goji/node_modules/@babel/parser/lib/index.js:13267:16)
    at Parser.parseVarStatement (/Users/malash/Projects/test-goji/node_modules/@babel/parser/lib/index.js:13100:10)
    at Parser.parseStatementContent (/Users/malash/Projects/test-goji/node_modules/@babel/parser/lib/index.js:12683:23)
    at Parser.parseStatementLike (/Users/malash/Projects/test-goji/node_modules/@babel/parser/lib/index.js:12588:17)
    at Parser.parseModuleItem (/Users/malash/Projects/test-goji/node_modules/@babel/parser/lib/index.js:12565:17)
    at Parser.parseBlockOrModuleBlockBody (/Users/malash/Projects/test-goji/node_modules/@babel/parser/lib/index.js:13189:36)
    at Parser.parseBlockBody (/Users/malash/Projects/test-goji/node_modules/@babel/parser/lib/index.js:13182:10)
    at Parser.parseProgram (/Users/malash/Projects/test-goji/node_modules/@babel/parser/lib/index.js:12464:10)
    at Parser.parseTopLevel (/Users/malash/Projects/test-goji/node_modules/@babel/parser/lib/index.js:12454:25)
    at Parser.parse (/Users/malash/Projects/test-goji/node_modules/@babel/parser/lib/index.js:14376:10)
    at parse (/Users/malash/Projects/test-goji/node_modules/@babel/parser/lib/index.js:14417:38)
    at parser (/Users/malash/Projects/test-goji/node_modules/@babel/core/lib/parser/index.js:41:34)
    at parser.next (<anonymous>)
    at parse (/Users/malash/Projects/test-goji/node_modules/@babel/core/lib/parse.js:25:37)
    at parse.next (<anonymous>)
    at evaluateSync (/Users/malash/Projects/test-goji/node_modules/gensync/index.js:251:28)
    at sync (/Users/malash/Projects/test-goji/node_modules/gensync/index.js:89:14)
    at stopHiding - secret - don't use this - v1 (/Users/malash/Projects/test-goji/node_modules/@babel/core/lib/errors/rewrite-stack-trace.js:47:12)
    at Object.parseSync (/Users/malash/Projects/test-goji/node_modules/@babel/core/lib/parse.js:40:72)
    at parseFile (/Users/malash/Projects/test-goji/node_modules/@linaria/babel-preset/lib/transform/Entrypoint.helpers.js:35:29)
    at /Users/malash/Projects/test-goji/node_modules/@linaria/babel-preset/lib/transform/Entrypoint.helpers.js:129:48
    at EventEmitter.perf (/Users/malash/Projects/test-goji/node_modules/@linaria/utils/lib/EventEmitter.js:45:20)
    at getOrParse (/Users/malash/Projects/test-goji/node_modules/@linaria/babel-preset/lib/transform/Entrypoint.helpers.js:129:24)
    at get ast [as ast] (/Users/malash/Projects/test-goji/node_modules/@linaria/babel-preset/lib/transform/Entrypoint.helpers.js:148:14)
    at BaseAction.explodeReexports (/Users/malash/Projects/test-goji/node_modules/@linaria/babel-preset/lib/transform/generators/explodeReexports.js:39:68)
    at explodeReexports.next (<anonymous>)
    at /Users/malash/Projects/test-goji/node_modules/@linaria/babel-preset/lib/transform/actions/BaseAction.js:66:78
    at EventEmitter.action (/Users/malash/Projects/test-goji/node_modules/@linaria/utils/lib/EventEmitter.js:25:22)
    at BaseAction.emitAction (/Users/malash/Projects/test-goji/node_modules/@linaria/babel-preset/lib/transform/actions/BaseAction.js:131:39)
    at nextFn (/Users/malash/Projects/test-goji/node_modules/@linaria/babel-preset/lib/transform/actions/BaseAction.js:66:32)
    at processNext (/Users/malash/Projects/test-goji/node_modules/@linaria/babel-preset/lib/transform/actions/BaseAction.js:111:28)
    at Object.next (/Users/malash/Projects/test-goji/node_modules/@linaria/babel-preset/lib/transform/actions/BaseAction.js:120:9)
    at syncActionRunner (/Users/malash/Projects/test-goji/node_modules/@linaria/babel-preset/lib/transform/actions/actionRunner.js:68:95)
    at syncActionRunner (/Users/malash/Projects/test-goji/node_modules/@linaria/babel-preset/lib/transform/actions/actionRunner.js:75:22)
    at syncActionRunner (/Users/malash/Projects/test-goji/node_modules/@linaria/babel-preset/lib/transform/actions/actionRunner.js:75:22)
    at transformSync (/Users/malash/Projects/test-goji/node_modules/@linaria/babel-preset/lib/transform.js:51:55)
    at PluginPass.pre (/Users/malash/Projects/test-goji/node_modules/@linaria/babel-preset/lib/plugins/babel-transform.js:42:36)
    at transformFile (/Users/malash/Projects/test-goji/node_modules/@babel/core/lib/transformation/index.js:73:27)
    at transformFile.next (<anonymous>)
    at run (/Users/malash/Projects/test-goji/node_modules/@babel/core/lib/transformation/index.js:24:12)
    at run.next (<anonymous>)
    at Function.<anonymous> (/Users/malash/Projects/test-goji/node_modules/@babel/core/lib/transform-file.js:27:33)
    at Generator.next (<anonymous>)
    at step (/Users/malash/Projects/test-goji/node_modules/gensync/index.js:261:32)
    at /Users/malash/Projects/test-goji/node_modules/gensync/index.js:273:13
    at async.call.result.err.err (/Users/malash/Projects/test-goji/node_modules/gensync/index.js:223:11)
    at /Users/malash/Projects/test-goji/node_modules/gensync/index.js:189:28
    at FSReqCallback.readFileAfterClose [as oncomplete] (node:internal/fs/read_file_context:68:3) {
  code: 'BABEL_PARSE_ERROR',
  reasonCode: 'DeclarationMissingInitializer',
  loc: Position { line: 1, column: 7, index: 7 },
  pos: 7
}
error Command failed with exit code 1.
info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.
```

## Good case

If you want to see the good case, you should checkout the `good-case` branch. The folder structure looks like this:

```
├── package.json
|── babel.config.json
├── src
│   └── index.ts
└── yarn.lock
```

As you can see, the only difference is that I added a `babel.config.json` file with the following content:

```json
{
  "presets": ["@babel/typescript", "@linaria"]
}
```

and now the `yarn start` command will run `babel src/index.ts` and output will be:

```
yarn run v1.22.19
$ babel src/index.ts
const a = 1;

✨  Done in 0.26s.
```

## Linaria 2

This bug is not present in Linaria 2. If you want to see the good case, you should checkout the `linaria-2` branch.

## Conclusion

I have no idea why this is happening, but I think it's a bug in the `@linaria/babel-preset` package. As I understand it, the `@linaria/babel-preset` package should be able to work with the `babel.config.json` file or `babel --presets` option, but it doesn't.

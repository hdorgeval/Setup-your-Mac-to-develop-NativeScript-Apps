### Configure TypeScript for your project {#configure-typescript-for-your-project}

The tsconfig.json file contains a default configuration of the TypeScript compiler.

For a Node.js or NativeScript project the tsconfig.json should look like :

```
{
    "compilerOptions": {
        "module": "commonjs",
        "moduleResolution": "node",
        "target": "es5",
        "sourceMap":true,
        "experimentalDecorators": true,
        "emitDecoratorMetadata": true
    }
}
```

More details on the compiler options at :

* [http://www.typescriptlang.org/docs/handbook/tsconfig-json.html](http://www.typescriptlang.org/docs/handbook/tsconfig-json.html)

* [http://www.typescriptlang.org/docs/handbook/compiler-options.html](http://www.typescriptlang.org/docs/handbook/compiler-options.html)




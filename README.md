JavaScript "pnpm" alias Demo
============================

"pnpm"中提供了alias功能，可以让我们对某一个package（甚至它的某一个版本）提供一个别名，方便使用（比如修bug等）。

如果我们运行了命令：

```
pnpm install --save lodash3@npm:lodash@^3.10.1
```

那么它就会在package.json的`dependencies`中增加：

```
"lodash3": "npm:lodash@^3.10.1"
```

那我们在代码中就可以`require('lodash3')`了。

需要注意的是，该功能仅被pnpm支持。如果你使用`npm install`的话，会提示错误。

# 深入理解 dva

> 源码版本：[2.4.1](https://github.com/dvajs/dva/tree/dva%402.4.1)

## const app = dva({}) 里做了什么？
```Javascript
// https://github.com/dvajs/dva/blob/dva%402.4.1/packages/dva/src/index.js

export default function (opts = {}) {

    // 1. 如果不传入 history 则创建一个新的 Hash History
    const history = opts.history || createHashHistory();

    // 2. ???
    const createOpts = {
        initialReducer: {
            routing, // import { routerReducer as routing, } from 'react-router-redux';
        },
        setupMiddlewares(middlewares) {
            return [
                routerMiddleware(history),
                ...middlewares,
            ];
        },
        setupApp(app) {
            app._history = patchHistory(history);
        },
    };

    // 3. ???
    const app = core.create(opts, createOpts);

    // 4. ???
    const oldAppStart = app.start;
    app.router = router;
    app.start = start;

    // 5. 
    return app;
}
```

### const app = core.create(opts, createOpts); 里做了什么？
```Javascript
// https://github.com/dvajs/dva/blob/dva%402.4.1/packages/dva-core/src/index.js

export function create(hooksAndOpts = {}, createOpts = {}) {

    // 1. ???
    const { initialReducer, setupApp = noop } = createOpts; // export const noop = () => {};

    // 2. ???
    const plugin = new Plugin();
    plugin.use(filterHooks(hooksAndOpts));

    // 3. ???
    const app = {
        _models: [prefixNamespace({ ...dvaModel })],
        _store: null,
        _plugin: plugin,
        use: plugin.use.bind(plugin),
        model,
        start,
    };
    return app;
}
```

## app.start() 里做了什么？
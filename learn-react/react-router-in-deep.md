# 深入理解 React Router

> 源码版本: [react-router v4.3.1](https://github.com/ReactTraining/react-router/releases/tag/v4.3.1)

## react-router-dom 

API
- 组件
    - 路由组件（router components）：BrowserRouter、HashRouter、MemoryRouter、StaticRouter、Router
    - 路径匹配组件（route matching components）：Route、Switch
    - 导航组件（navigation components）：Link、NavLink、Redirect、Prompt
- 工具函数：generatePath、matchPath、withRouter

## connected-react-router
> 源码: [connected-react-router v6.3.1](https://github.com/supasate/connected-react-router/tree/v6.3.1)

\<ConnectedRouter\> 组件必须传入属性 `history`

## 参考资料
- [前端路由实现及 react-router v4 源码分析](https://github.com/fi3ework/blog/issues/21) by fi3ework
- [React Router v4 几乎误我一生](https://zhuanlan.zhihu.com/p/27433116) by 程墨Morgan
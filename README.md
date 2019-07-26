# HR365
- [HR365 前端开发指南](hr365-web-dev-guides/index.md)

# 团队协作
- Subversion（简称 svn），集中式版本控制工具
    - 官网: [http://subversion.apache.org](http://subversion.apache.org)
    - svn server
        - [VisualSVN](https://www.visualsvn.com/server/) for Windows
    - svn client
        - [TortoiseSVN](https://tortoisesvn.net) for Windows，免费
        - [Cornerstone](https://cornerstone.assembla.com) for macOS，付费
        - [SmartSVN](https://www.smartsvn.com) for macOS, Windows and Linux，付费
    - diff & merge tool
        - [Beyond Compare](https://www.scootersoftware.com)，付费
        - [diffmerge](https://sourcegear.com/diffmerge/) for macOS, Windows and Linux，免费
    - 核心概念
        - 签出 checkout，将服务器代码下载到本地，同时带版本控制信息（.svn 文件）
        - 导出 export，将服务器代码备份到本地，不带版本控制信息
        - 提交 commit，将修改的代码上传到服务器
        - 更新 update，将别人修改的代码下载到本地
        - 合并 merge
        - 冲突 conflict
    - 工作流
        - [svn 工作流管理个人实践](http://solnotes.com/2015/05/04/svn-workflow-management/) by sol_catdog 2015-05
- OKR

# 前端开发
- HTML
    - 标准
        - HTML4.1
        - XHTML
        - [HTML5](https://www.w3.org/TR/2014/REC-html5-20141028/)
- CSS
    - 标准
        - [Cascading Style Sheets Level 2 Revision 1](https://www.w3.org/TR/CSS2/)
- JavaScript
    - [如何学习 JavaScript](how-to-learn-js.md)
    - [JavaScript 运行环境](js-env.md)
    - [数据类型](js-type.md)
    - [立即执行函数 IIEF](js-iief.md)
- DOM
- React
    - [React 最佳实践](react-best-practices.md)
    - Redux
    - Redux Saga
    - React Router
    - Dva 框架
    - Ant Design 组件库
- 工具链
    - Node.js
        - path
        - fs
        - child_process
        - express
        - 编写命令行工具必备
            - [chalk](https://github.com/chalk/chalk)
            - 命令解析: [commander](https://github.com/tj/commander.js) / [yargs](https://github.com/yargs/yargs)
            - ...
    - npm / yarn
        - [版本号管理策略 && 使用 npm 管理项目版本号](http://buzhundong.com/post/版本号管理策略-使用npm管理项目版本号.html)
    - Babel
    - ESLint
    - Bundler
        - Webpack
        - Metro
        - Rollup
    - Grunt / Gulp
    - Flow
    - TypeScript
    - create-react-app
    - roadhog
        - [roadhog 工作原理](how-roadhog-works.md)
    - umi
    - electron
- 浏览器原理
    - 【必读】[How Browsers Work: Behind the scenes of modern web browsers](https://www.html5rocks.com/en/tutorials/internals/howbrowserswork/) by Tali Garsiel & Paul Irish, 2011
- 安全
    - 跨站脚本攻击 XSS
        - [前端安全系列（一）：如何防止XSS攻击？](https://juejin.im/post/5bad9140e51d450e935c6d64) by 美团技术团队 2018-09
    - 跨站请求伪造 CSRF
        - [前端安全系列（二）：如何防止CSRF攻击？](https://juejin.im/post/5bc009996fb9a05d0a055192) by 美团技术团队 2018-10

# 移动端开发
- iOS 开发
    - 苹果开发者账号
    - 编程语言：Objective-C、Swift
    - 构建系统
        - CocoaPods
- Android 开发
    - 编程语言：Java、Kotlin
    - 构建系统
        - Gradle
- 小程序
    - 微信小程序
    - 支付宝小程序
- 跨端方案
    - React Native
        - Networking
            - XMLHttpRequest (XHR)
                - [API](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest)
            - Fetch
                - [API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)
            - WebSockets
                - [API](https://developer.mozilla.org/en-US/docs/Web/API/WebSocket)
                - 源码: [iOS](https://github.com/facebook/react-native/tree/master/Libraries/WebSocket) | [Android](https://github.com/facebook/react-native/tree/master/ReactAndroid/src/main/java/com/facebook/react/modules/websocket)
            - [Network layer in React Native](https://medium.com/dailyjs/network-layer-in-react-native-eec841f11861) by Kureev Alexey, 2017
        - react-navigation
        - react-native-image-picker
        - react-native-svg
        - Ant Design Mobile RN 组件库
        - 键盘遮挡
            - [React Native Keyboard Covering Inputs](https://codeburst.io/react-native-keyboard-covering-inputs-72a9d3072689) by John Tucker
    - Flutter
    - Chameleon
    - Taro

# 服务端开发
- Java
- ...

# 网络
- TCP
- SSL / TLS
- HTTP
    - HTTP/1.1
        - [RFC7230: Message Syntax and Routing](https://tools.ietf.org/html/rfc7230)
        - [RFC7231: Semantics and Content](https://tools.ietf.org/html/rfc7231)
        - [RFC7232: Conditional Requests](https://tools.ietf.org/html/rfc7232)
        - [RFC7233: Range Requests](https://tools.ietf.org/html/rfc7233)
        - [RFC7234: Caching](https://tools.ietf.org/html/rfc7234)
        - [RFC7235: Authentication](https://tools.ietf.org/html/rfc7235)
    - HTTPS
    - HTTP/2
- WebSocket
    - [RFC6455: The WebSocket Protocol](https://tools.ietf.org/html/rfc6455) | [中文](https://juejin.im/post/5c6b7366e51d45016527d648)
    - [WebSocket API](https://developer.mozilla.org/en-US/docs/Web/API/WebSocket)
- OAuth
- XMPP

# 运维 DevOps
- Linux
- 基础服务搭建
    - Nignx
    - [Nexus OSS](https://www.sonatype.com/nexus-repository-oss)
- 数据库
    - MySQL
    - Redis
- 监控
- 安全

# UI / UX
- Sketch
    - 工具箱
        - [Kitchen](http://kitchen.alipay.com)
    - 标注
        - [sketch-measure](https://github.com/utom/sketch-measure)
        - [marketch](https://github.com/tudou527/marketch)
        - [zeplin](https://zeplin.io)（付费）
    - 汉化
        - [SketchI18N](https://github.com/cute/SketchI18N)
- 设计系统 Design System

# 前沿
- 人工智能
    - 基础数学
        - 线性代数
        - 概率论
        - 数理统计
        - 信息论
    - 方法论
        - 机器学习
        - 深度学习
        - 神经网络
    - 应用场景
        - 计算机视觉
        - 自然语言分析
- 区块链

# 资料
- [工具](tools.md)
- [收录高质量技术博客](blogs.md)

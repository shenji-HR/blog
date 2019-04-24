# 发布

## 1. 发布 hr365-ws-api

第一步，svn checkout https://192.168.1.118:1443/svn/hr365/HRCODE/Basic/Client

第二步，将最新的后台接口 excel 配置文件复制到 `Client/hr365-ws-api/branches/dev/scripts` 目录下

第三步，cd 到 `Client/scripts` 目录下，执行 pub-hr365-ws-api.sh 脚本。注：由于 hr365-model 下的所有子包都依赖 hr365-ws-api，而 hr365-basic 又依赖 hr365-model，因此发布 hr365-ws-api 的同时，也会发布 hr365-model 和 hr365-basic。

第四步，app 工程执行 `yarn add @shenji/hr365-basic` 升级依赖。

## 附：@shenji 域下包依赖关系概览
- @shenji/hr365-basic
    - @shenji/hr365-basic-model
        - @shenji/hr365-ws-api
            - @shenji/hr365-util
    - @shenji/hr365-exp-model
        - @shenji/hr365-ws-api
            - @shenji/hr365-util
    - @shenji/hr365-hr-model
        - @shenji/hr365-ws-api
            - @shenji/hr365-util
    - @shenji/hr365-pay-model
        - @shenji/hr365-ws-api
            - @shenji/hr365-util
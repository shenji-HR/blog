# 发布

## 1. 发布 hr365-ws-api

第一步， npm 没有登录过的需要先执行 `npm login -registry=http://172.30.3.107:8082/repository/npm_hosted/`，用户名、密码为自己名字的拼音缩写，例如 jyx；邮箱可以填公司邮箱，例如 yourname@21esn.com

第二步，svn checkout https://192.168.1.118:1443/svn/hr365/HRCODE/Basic/Client

第三步，将最新的后台接口 excel 配置文件复制到 `Client/hr365-ws-api/branches/dev/scripts` 目录下

第四步，cd 到 `Client/scripts` 目录下，执行 `sh pub-hr365-ws-api.sh` 运行脚本。注：由于 hr365-model 下的所有子包都依赖 hr365-ws-api，而 hr365-basic 又依赖 hr365-model，因此发布 hr365-ws-api 的同时，也会发布 hr365-model 和 hr365-basic。

第五步，app 工程执行 `yarn add @shenji/hr365-basic` 升级依赖。

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

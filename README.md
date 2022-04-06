亿洽
=======

亿洽 是一个基于Element-Web(https://github.com/vector-im/element-web) 构建的一个社区分支。

支持环境
======================


* 操作系统
  * macOS
  * Windows
  * Linux
* 浏览器
  * 亿洽可以安装 Chrome, Firefox, 和 Safari的web端

开始
===============

亿洽官网: <https://yiqia.com/>

亿洽Web: <https://app.yiqia.com/>


安装亿洽桌面程序，参考下面的 [桌面端安装](#running-as-a-desktop-app)。

运行桌面端
========================

亿洽能用electron包装并运行在桌面端，你可以从 <https://github.com/eachchat/yiqia-desktop/release>下载一个预先构建的版本。

自己构建需要参考 <https://github.com/eachchat/yiqia-desktop>.


设置一个开发环境
============================

下载并编译 `matrix-js-sdk`:

``` bash
git clone https://github.com/eachchat/matrix-js-sdk.git
pushd matrix-js-sdk
yarn link
yarn install
popd
```


```bash
git clone https://github.com/eachchat/yiqia-react-sdk.git
pushd matrix-react-sdk
yarn link
yarn link matrix-js-sdk
yarn install
popd
```


```bash
git clone https://github.com/eachchat/yiqia-web.git
cd yiqia-web
yarn link matrix-js-sdk
yarn link matrix-react-sdk
yarn install
yarn reskindex
yarn start
```



___

当你完成 `matrix-react-sdk` 和 `matrix-js-sdk` 的修改，需要自动构建和打包.

如果你从亿洽移除了一些组件，你需要重新打包。


运行测试程序
-----------------

有一些测试用例在 `tests` 文件夹，这些被设计使用 Jest and JSDOM 运行。运行他们需要执行

```
yarn test
```

<<<<<<< HEAD
### End-to-End 测试
=======
### End-to-End tests

See [matrix-react-sdk](https://github.com/matrix-org/matrix-react-sdk/#end-to-end-tests) for how to run the end-to-end tests.
>>>>>>> v1.10.8

根据 [matrix-react-sdk](https://github.com/matrix-org/matrix-react-sdk/#end-to-end-tests) 怎样运行end-to-end测试.



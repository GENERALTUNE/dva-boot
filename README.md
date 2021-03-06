# DVA-BOOT

使用dva 2以及React 16，动态路由，目录按功能划分，开发时不用关心其它目录，只在自已的路由下写新功能即可，配置也都在自已的目录中，团队成员开发不会互相冲突。

```
.
├── .vscode                  # VSCode 相关设置
├── public                   # 不参与编译的资源文件
├── src                      # 主程序目录
│   ├── index.js             # 程序启动和渲染入口文件
│   ├── components           # 全局公共组件
│   ├── layouts              # 页面结构组件
│   │   ├── BasicLayout      # 基本布局
│   │   └── OtherLayout      # 布局组件根据具体功能调整，在路由配置中引用
│   ├── routes               # 动态路由目录（每个功能一个文件夹的MVC结构）
│   │   ├── index.js         # 路由配置文件
│   │   ├── Home             # 功能模块
│   │   │   ├── index.js     # 路由配置文件
│   │   │   ├── assets       # 单独属于这个模块的静态资源文件
│   │   │   ├── components   # 页面组件
│   │   │   ├── model        # dva model
│   │   │   ├── service      # dva service
│   │   │   └── routes **    # 子路由(目录结构与父级相同)
│   │   └── Login            # 功能模块
│   │       ├── index.js     # 路由配置文件
│   │       ├── assets       # 单独属于这个模块的静态资源文件
│   │       ├── components   # 页面组件
│   │       ├── model        # dva model
│   │       ├── service      # dva service
│   │       └── routes **    # 子路由(目录结构与父级相同)
│   ├── utils                # 工具类
│   └── assets               # 资源文件
│           ├── fonts        # 字体 & 字体图标
│           ├── images       # 图片
│           └── styles       # 全局样式
```

## 使用

```bash
$ git clone https://github.com/LANIF-UI/dva-boot.git
$ cd dva-boot
$ yarn
$ yarn start
```

## 参考资料
- [create-react-app](https://github.com/facebookincubator/create-react-app)
- [dvajs](https://github.com/dvajs/dva)
- [react-script-antd-pro](https://github.com/WhatAKitty/react-script-antd-pro/tree/master/src)
- [react-redux-starter-kit](https://github.com/davezuko/react-redux-starter-kit)
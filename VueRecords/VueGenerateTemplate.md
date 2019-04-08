# Vue 生成初始模板

## 创建一个Vue项目 ##
创建的样例可以参考之前已经做过的项目:
1. [Github liyf7218/pro-vue](https://github.com/liyf7218/pro-vue), 这是最初进行测试的项目,已经停更,仅供参考.
2. [Github whutAutoSquad/FE_ProgressiveProject](https://github.com/whutAutoSquad/FE_ProgressiveProject), 这个项目中是在前一个项目的基础上搭建继续开发的,添加了更多的插件,也提供参考.
3. 如果开发,建议直接跳转到  "使用vue/cli-init搭建".

### 基础知识 ###
1. 安装Node.js,请查看 [nodejs 官网](http://nodejs.cn/),建议将npm源替换为国内源,如 [淘宝NPM镜像 cnpm](http://npm.taobao.org/)
2. 熟悉vue的概念和相关组件,请查看 [Vue 官网](https://cn.vuejs.org/)
3. 遵循官网的建议,使用官方创建工具 *vue-cli* 进行项目搭建.在这里进行简单的讲解,更多详情可访问 [vue-cli 官网](https://cli.vuejs.org/)

### 开始搭建 ###
安装 vue-cli:

```
$ npm install -g @vue/cli
$ vue --version
  3.4.0
```

生成项目:

```
$ vue create vue_workspace
? Please pick a preset: (Use arrow keys)
? Please pick a preset: default (babel, eslint)
? Pick the package manager to use when installing dependencies: (Use arrow keys)
? Pick the package manager to use when installing dependencies: Yarn
-  Creating project in D:\workspace\liyf_studio\vue_workspace.
✨  Creating project in D:\workspace\liyf_studio\vue_workspace.
⚙  Installing CLI plugins. This might take a while...
----
yarn install v1.13.0
info No lockfile found.
[1/4] Resolving packages...
[2/4] Fetching packages...
info fsevents@1.2.7: The platform "win32" is incompatible with this module.
info "fsevents@1.2.7" is an optional dependency and failed compatibility check. Excluding it from installation.
[3/4] Linking dependencies...
[4/4] Building fresh packages...
success Saved lockfile.
Done in 76.45s.
  Invoking generators...
  Installing additional dependencies...
----
yarn install v1.13.0
[1/4] Resolving packages...
[2/4] Fetching packages...
info fsevents@1.2.7: The platform "win32" is incompatible with this module.
info "fsevents@1.2.7" is an optional dependency and failed compatibility check. Excluding it from installation.
[3/4] Linking dependencies...
[4/4] Building fresh packages...
success Saved lockfile.
Done in 19.12s.
-  Running completion hooks...
⚓  Running completion hooks...
----
-  Generating README.md...
  Generating README.md...
----
  Successfully created project vue_workspace.
  Get started with the following commands:
----
 $ cd vue_workspace
 $ yarn serve
```

此处可能会用到yarn,安装命令如下:

```
$ cnpm i -g yarn
```

运行项目

先查看package.json中的命令项,可以看到有:

> ...
> "scripts": {
>   "serve": "vue-cli-service serve",
>   "build": "vue-cli-service build",
>   "lint": "vue-cli-service lint"
> },
> ...

执行命令:

```

$ npm run serve

 vue_workspace@0.1.0 serve D:\workspace\liyf_studio\vue_workspace
 vue-cli-service serve

 INFO  Starting development server...
 98% after emitting CopyPlugin DONE  Compiled successfully in 4091ms14:18:03


  App running at:
   Local:   http://localhost:8080/
   Network: http://10.0.56.88:8080/

  Note that the development build is not optimized.
  To create a production build, run yarn build.

```

然后打开浏览器,打开 [ http://localhost:8080/ ](http://localhost:8080/),即可进入vue demo页面:

![图片](https://dev.tencent.com/api/project/4121910/files/4667986/imagePreview)

至此,一个vue demo搭建完成.
查看package.json

```
$ cat package.json
{
  "name": "vue_workspace",
  "version": "0.1.0",
  "private": true,
  "scripts": {
    "serve": "vue-cli-service serve",
    "build": "vue-cli-service build",
    "lint": "vue-cli-service lint"
  },
  "dependencies": {
    "vue": "^2.5.22"
  },
  "devDependencies": {
    "@vue/cli-plugin-babel": "^3.4.0",
    "@vue/cli-plugin-eslint": "^3.4.0",
    "@vue/cli-service": "^3.4.0",
    "babel-eslint": "^10.0.1",
    "eslint": "^5.8.0",
    "eslint-plugin-vue": "^5.0.0",
    "vue-template-compiler": "^2.5.21"
  },
  "eslintConfig": {
    "root": true,
    "env": {
      "node": true
    },
    "extends": [
      "plugin:vue/essential",
      "eslint:recommended"
    ],
    "rules": {},
    "parserOptions": {
      "parser": "babel-eslint"
    }
  },
  "postcss": {
    "plugins": {
      "autoprefixer": {}
    }
  },
  "browserslist": [
    "> 1%",
    "last 2 versions",
    "not ie <= 8"
  ]
}
```

可见这样创建的demo,没有引入常用的工具,知识单纯的创建了一个vue页面,如果需要更加丰富的功能,进行下一步.

### 使用vue/cli-init搭建 ###
执行命令:

```
$ vue init webpack vue_webpack_workspace

  Command vue init requires a global addon to be installed.
  Please run yarn global add @vue/cli-init and try again.
```

根据提示引入 vue/cli-init.

```
$ yarn global add @vue/cli-init
yarn global v1.13.0
[1/4] Resolving packages...
warning @vue/cli-init > vue-cli > coffee-script@1.12.7: CoffeeScript on NPM has moved to "coffeescript" (no hyphen)
warning @vue/cli-init > vue-cli > metalsmith > gray-matter > coffee-script@1.12.7: CoffeeScript on NPM has moved to "coffeescript" (no hyphen)
[2/4] Fetching packages...
[3/4] Linking dependencies...
[4/4] Building fresh packages...
warning "@vue/cli-init@3.4.0" has no binaries
Done in 42.36s.
```

再执行命令:

```
$ vue init webpack vue_webpack_workspace

  Command vue init requires a global addon to be installed.
  Please run yarn global add @vue/cli-init and try again.
```

发现还是报一样的错误.
所以查看一下官网,根据官网的步骤进行安装,如下:

![图片](https://dev.tencent.com/api/project/4121910/files/4670388/imagePreview)

```
$ cnpm i -g @vue/cli-init
Downloading @vue/cli-init to C:\Users\李叶飞\AppData\Roaming\npm\node_modules\@vue\cli-init_tmp
[npminstall:get] retry GET https://registry.npm.taobao.org/@vue%2Fcli-init after 100ms, retry left 4, error: ResponseTimeoutError: Response timeout for 60000ms, GET https://registry.npm.taobao.org/@vue%2Fcli-init -1 (connected: true, keepalive socket:false, agent status: {"createSocketCount":2,"createSocketErrorCount":0,"closeSocketCount":2,"errorSocketCount":0,"timeoutSocketCount":0,"requestCount":2,"freeSockets":{},"sockets":{},"requests":{}}, socketHandledRequests: 1, socketHandledResponses: 0)
headers: {}, status: -1, headers: {},
stack: ResponseTimeoutError: Response timeout for 60000ms, GET https://registry.npm.taobao.org/@vue%2Fcli-init -1 (connected: true, keepalive socket: false, agent status: {"createSocketCount":2,"createSocketErrorCount":0,"closeSocketCount":2,"errorSocketCount":0,"timeoutSocketCount":0,"requestCount":2,"freeSockets":{},"sockets":{},"requests":{}}, socketHandledRequests: 1, socketHandledResponses: 0)
headers: {}
    at Timeout._onTimeout (C:\Users\李叶飞\AppData\Roaming\npm\node_modules\cnpm\node_modules\urllib\lib\urllib.js:835:15)
    at ontimeout (timers.js:425:11)
    at tryOnTimeout (timers.js:289:5)
    at listOnTimeout (timers.js:252:5)
    at Timer.processTimers (timers.js:212:10)
Copying C:\Users\李叶飞\AppData\Roaming\npm\node_modules\@vue\cli-init_tmp\_@vue_cli-init@3.4.0@@vue\cli-init to C:\Users\李叶飞\AppData\Roaming\npm\node_modules\@vue\cli-init
Installing @vue/cli-init's dependencies to C:\Users\李叶飞\AppData\Roaming\npm\node_modules\@vue\cli-init/node_modules
[1/2] execa@^1.0.0 installed at node_modules\_execa@1.0.0@execa
[2/2] vue-cli@^2.9.2 installed at node_modules\_vue-cli@2.9.6@vue-cli
deprecate vue-cli@2.9.6 › metalsmith@2.3.0 › gray-matter@2.1.1 › coffee-script@^1.12.4 CoffeeScript on NPM has moved to "coffeescript" (no hyphen)
Recently updated (since 2019-02-07): 4 packages (detail see file C:\Users\李叶飞\AppData\Roaming\npm\node_modules\@vue\cli-init\node_modules\.recently_updates.txt)
  2019-02-13
    → vue-cli@2.9.6 › async@^2.4.0(2.6.2) (06:36:10)
  2019-02-10
    → vue-cli@2.9.6 › request@2.88.0 › har-validator@5.1.3 › ajv@^6.5.5(6.9.1) (16:42:28)
  2019-02-08
    → vue-cli@2.9.6 › download-git-repo@1.1.0 › download@5.0.3 › decompress@4.2.0 ›decompress-tarbz2@4.1.1 › unbzip2-stream@^1.0.9(1.3.3) (23:11:06)
  2019-02-07
    → vue-cli@2.9.6 › handlebars@^4.0.5(4.1.0) (17:48:59)
All packages installed (252 packages installed from npm registry, used 13s(network 13s), speed 403.16kB/s, json 235(411.33kB), tarball 4.76MB)
```

安装完成,接下来进行项目创建:

```
$ vue init webpack vue_webpack_workspace

? Project name (vue_webpack_workspace)
? Project name vue_webpack_workspace
? Project description (A Vue.js project)
? Project description A Vue.js project
? Author (liyf7218 <liyf7218@163.com>)
? Author liyf7218 <liyf7218@163.com>
? Vue build runtime
? Install vue-router? (Y/n) Y
? Install vue-router? Yes
? Use ESLint to lint your code? (Y/n) n
? Use ESLint to lint your code? No
? Set up unit tests (Y/n) Y
? Set up unit tests Yes
? Pick a test runner (Use arrow keys)
? Pick a test runner jest
? Setup e2e tests with Nightwatch? (Y/n)
? Setup e2e tests with Nightwatch? Yes
? Should we run `npm install` for you after the project has been created? (recom
? Should we run `npm install` for you after the project has been created? (recom
mended) npm

   vue-cli · Generated "vue_webpack_workspace".


# Installing project dependencies ...
# ========================

npm WARN deprecated browserslist@2.11.3: Browserslist 2 could fail on reading Browserslist >3.0 config used in other tools.
npm WARN deprecated bfj-node4@5.3.1: Switch to the `bfj` package for fixes and new features!
npm WARN deprecated browserslist@1.7.7: Browserslist 2 could fail on reading Browserslist >3.0 config used in other tools.
npm WARN deprecated socks@1.1.10: If using 2.x branch, please upgrade to at least 2.1.6 to avoid a serious bug with socket data flow and an import issue introduced in 2.1.0

> chromedriver@2.46.0 install D:\workspace\liyf_studio\vue_webpack_workspace\node_modules\chromedriver
> node install.js

Current existing ChromeDriver binary is unavailable, proceding with download and extraction.
Downloading from file:  https://chromedriver.storage.googleapis.com/2.46/chromedriver_win32.zip
Saving to file: C:\Users\李叶飞\AppData\Local\Temp\2.46\chromedriver\chromedriver_win32.zip
Received 781K...
Received 1578K...
Received 2362K...
Received 3146K...
Received 3930K...
Received 4523K total.
Extracting zip contents
Copying to target path D:\workspace\liyf_studio\vue_webpack_workspace\node_modules\chromedriver\lib\chromedriver
Done. ChromeDriver binary available at D:\workspace\liyf_studio\vue_webpack_workspace\node_modules\chromedriver\lib\chromedriver\chromedriver.exe

> uglifyjs-webpack-plugin@0.4.6 postinstall D:\workspace\liyf_studio\vue_webpack_workspace\node_modules\webpack\node_modules\uglifyjs-webpack-plugin
> node lib/post_install.js

npm notice created a lockfile as package-lock.json. You should commit this file.
npm WARN optional SKIPPING OPTIONAL DEPENDENCY: fsevents@1.2.7 (node_modules\fsevents):
npm WARN notsup SKIPPING OPTIONAL DEPENDENCY: Unsupported platform for fsevents@1.2.7: wanted {"os":"darwin","arch":"any"} (current: {"os":"win32","arch":"x64"})

added 1491 packages from 1076 contributors and audited 30412 packages in 154.382s
found 8 vulnerabilities (1 low, 1 moderate, 5 high, 1 critical)
  run `npm audit fix` to fix them, or `npm audit` for details

# Project initialization finished!
# ========================

To get started:

  cd vue_webpack_workspace
  npm run dev

Documentation can be found at https://vuejs-templates.github.io/webpack
```

此时创建完成,运行项目

```
$ npm start

> vue_webpack_workspace@1.0.0 start D:\workspace\liyf_studio\vue_webpack_workspace
> npm run dev

> vue_webpack_workspace@1.0.0 dev D:\workspace\liyf_studio\vue_webpack_workspace
> webpack-dev-server --inline --progress --config build/webpack.dev.conf.js
...
 I  Your application is running here: http://localhost:8080
```

用浏览器打开 localhost:8080,可见:

![图片](https://dev.tencent.com/api/project/4121910/files/4670418/imagePreview)

查看package.json

```
$ cat package.json
{
  "name": "vue_webpack_workspace",
  "version": "1.0.0",
  "description": "A Vue.js project",
  "author": "liyf7218 <liyf7218@163.com>",
  "private": true,
  "scripts": {
    "dev": "webpack-dev-server --inline --progress --config build/webpack.dev.conf.js",
    "start": "npm run dev",
    "unit": "jest --config test/unit/jest.conf.js --coverage",
    "e2e": "node test/e2e/runner.js",
    "test": "npm run unit && npm run e2e",
    "build": "node build/build.js"
  },
  "dependencies": {
    "vue": "^2.5.2",
    "vue-router": "^3.0.1"
  },
  "devDependencies": {
    "autoprefixer": "^7.1.2",
    "babel-core": "^6.22.1",
    "babel-helper-vue-jsx-merge-props": "^2.0.3",
    "babel-jest": "^21.0.2",
    "babel-loader": "^7.1.1",
    "babel-plugin-dynamic-import-node": "^1.2.0",
    "babel-plugin-syntax-jsx": "^6.18.0",
    "babel-plugin-transform-es2015-modules-commonjs": "^6.26.0",
    "babel-plugin-transform-runtime": "^6.22.0",
    "babel-plugin-transform-vue-jsx": "^3.5.0",
    "babel-preset-env": "^1.3.2",
    "babel-preset-stage-2": "^6.22.0",
    "babel-register": "^6.22.0",
    "chalk": "^2.0.1",
    "chromedriver": "^2.27.2",
    "copy-webpack-plugin": "^4.0.1",
    "cross-spawn": "^5.0.1",
    "css-loader": "^0.28.0",
    "extract-text-webpack-plugin": "^3.0.0",
    "file-loader": "^1.1.4",
    "friendly-errors-webpack-plugin": "^1.6.1",
    "html-webpack-plugin": "^2.30.1",
    "jest": "^22.0.4",
    "jest-serializer-vue": "^0.3.0",
    "nightwatch": "^0.9.12",
    "node-notifier": "^5.1.2",
    "optimize-css-assets-webpack-plugin": "^3.2.0",
    "ora": "^1.2.0",
    "portfinder": "^1.0.13",
    "postcss-import": "^11.0.0",
    "postcss-loader": "^2.0.8",
    "postcss-url": "^7.2.1",
    "rimraf": "^2.6.0",
    "selenium-server": "^3.0.1",
    "semver": "^5.3.0",
    "shelljs": "^0.7.6",
    "uglifyjs-webpack-plugin": "^1.1.1",
    "url-loader": "^0.5.8",
    "vue-jest": "^1.0.2",
    "vue-loader": "^13.3.0",
    "vue-style-loader": "^3.0.1",
    "vue-template-compiler": "^2.5.2",
    "webpack": "^3.6.0",
    "webpack-bundle-analyzer": "^2.9.0",
    "webpack-dev-server": "^2.9.1",
    "webpack-merge": "^4.1.0"
  },
  "engines": {
    "node": ">= 6.0.0",
    "npm": ">= 3.0.0"
  },
  "browserslist": [
    "> 1%",
    "last 2 versions",
    "not ie <= 8"
  ]
}
```

可见已经添加了多种脚手架工具,我们使用这个作为开发的基础,进行进一步的开发.

## 这个项目是啥
Vue 移动端新项目模板，封装了 H5 项目开发中一些比较常用的功能，比如：微信授权及分享、axios 封装、移动端 vw 适配、UI 组件库等等。
## 为什么会有这个项目
本人从事前端开发工作已有四年，这期间做的大部分都是移动端 H5 项目，这几年来大大小小的 H5 项目也做了有十几个了。
对于移动端 H5 项目来说，有些功能和配置其实是通用的，基本上每个项目都会用到，比如说：微信授权及分享、UI 组件库、各种小组件等。
基于我平时比较喜欢总结以及为了以后开发 H5 项目省事的目的，就有了这个项目（主要就是为了偷懒，，，）

## 特色功能
- 微信网页授权和分享
- 本人常用的几个公共 css
- 使用 less 进行 css 预编译
- 几个移动端开发中可能会用到的组件
- 开发环境下引入 vconsole 进行调试
- axios 封装，拦截器配置，接口定义模块
- postcss-px-to-viewport 移动端适配
- 已写好 eventBus 基础代码，按照说明即可直接使用
- 移动端组件库 vantUI，按需加载并全局引入了几个常用组件
- 已写好 App 底部导航 AppNavBar 组件，可自行对其进行调整
- 自定义指令、过滤器、utils 都已写好几个基本的模版，可根据需要增减
- 加入打包脚本 build.js，打包时会自动将版本号 +1，并压缩成 zip 包后放入 packages 文件夹中

## 使用方法
1. 直接 Download zip 包到本地（推荐）
推荐使用此方式使用本项目，直接 Download 本项目 zip 包到本地，解压后按照下面文档中提到的几个修改点进行相应的修改，修改完成后
运行 npm install 安装好各项依赖包之后就可以直接进行业务开发了
2. 自己创建新项目然后修改
想自己创建新项目，然后再进行配置也可以。首先用 vue-cli 创建一个全新的项目，然后将我这个项目里面的
 public 和 src 文件夹以及各配置文件复制到新项目目录下替换掉。再按照下面文档中提到的几个修改点进行相应的修改，修改完成后
运行 npm install 安装好各项依赖包之后就可以直接进行业务开发了
3. 老项目改造
老项目的话就只能自己根据需要将我这项目里的对你有用的东西的东西直接复制到你的项目内使用了

### 有改动的配置文件
1. 新增 build.js， 此文件是我写的一个打包脚本，作用就是在 build 时会自动将版本号 +1 且会生成相应的 zip 包，文件内有注释，不难看懂。
在 package.json 中我新增了一个 zip 命令，使用 npm run zip 即可调用该脚本自动打 zip 包
2. 新增 postcss.config.js，该文件是因为我引入了 postcss-px-to-viewport 来做移动端适配而增加的相应的配置文件。如果不用
该插件的话直接删掉该文件即可，或者自己根据需要修改配置 
3. babel.config.js，这是为了按需加载 vantUI 而配置的，如果没有使用任何组件库或者组件库不做按需加载，此文件不用修改，
当然如果你使用了其它组件库，请按照其提供的文档进行相应的配置
4. vue.config.js，这里修改了 publicPath、开启了 GZip 压缩和图片压缩，文件内都有注释，不需要的也可以都不改

### 需要修改的文件
上面是有改动的几个配置文件，下面是正式开发前还需要修改的几个地方
1. router.js 中 beforeEach 钩子函数中请求微信授权的代码，需要根据项目需要替换掉 appId，redirectUrl 等内容
2. utils 文件夹下 wxShare 文件，这里是对微信分享的封装代码，需要根据项目将里面的 url 等一些参数和处理逻辑改掉
3. apis 文件夹下 request 文件，根据项目需要换掉 BASE_URL 和拦截器里面相关配置
4. public 文件夹下 index.html 文件中的 title 内容根据不同项目改掉
5. public 文件夹下 favicon.ico 文件，根据项目需要换掉，（显示在浏览器标签上的网站 logo）
6. package.json 文件中 name 字段的值换掉
7. vue.config.js 文件中 publicPath 需要根据服务器目录做适当更改
8. 最后，记得修改项目根目录文件夹名字

**项目中各处需要修改的地方都加了 todo 注释，也可以全局搜索 todo 来修改
以上内容改完，整个项目框架基本就成型了，运行 npm install 安装好各项依赖包之后就可以直接进行业务开发了**

**如果觉得这个项目对你有帮助，烦请点下 star，同时也欢迎大家给我提意见和建议，共同学习和提高，感谢！**

## 我是谁
85年生人，已经被现实捶打了无数遍的中年社畜。30 岁时通过自学的方式从外贸行业转行进入 IT 编程领域，最初是做 Android 开发，后转入前端领域。以后打算专注于前端领域，正在往资深前端方向努力

如有需要，可通过下面微信二维码与我联系

![微信图片_20200919231413](https://img-blog.csdnimg.cn/2020091923290113.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3pnaDA3MTE=,size_16,color_FFFFFF,t_70#pic_center)

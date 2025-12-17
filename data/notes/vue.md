# vue
#### 简介：vue是一种用于构建用户界面的渐进式框架（渐进式就是可以在原有基础上根据需要逐步添加功能，根据项目需求和规模，以不同的方式集成到项目中去）
### 项目开发优势：
1. 轻量级
2. 基于<font style="color:#DF2A3F;">JavaScript</font>语言开发
3. 使用灵活
4. 减少对DOM直接操作，通过<font style="color:#DF2A3F;">API</font>来响应数据绑定（支持单向和双向）
5. 支持<font style="color:#DF2A3F;">组件化开发</font>（组件化开发：<font style="color:rgba(0, 0, 0, 0.85);">将一个功能拆解为多个独立的小功能，各个功能可以进行组合和交互，最终构建出完整的功能，不仅仅局限于功能，还有界面拆分和组合等</font>）拆解时<font style="color:rgba(0, 0, 0, 0.85);">合理规划组件的划分粒度</font>
6. 可与前端开发用到的一系列工具结合使用

### 特性：
1. <font style="color:#DF2A3F;">数据驱动视图</font>

<font style="color:rgb(24, 30, 51);">在使用Vue的页面中，Vue会监听数据变化。当页面数据发生变化时，Vue会自动重新渲染页面结构</font>

![画板](https://cdn.nlark.com/yuque/0/2025/jpeg/56055817/1746614670137-01b0d981-ecf3-4830-8bd3-4df051d64f07.jpeg)

2. <font style="color:#DF2A3F;">双向数据绑定</font>

数据发生改变，视图发生改变；视图发生改变，数据发生改变（视图：呈现在用户面前的页面界面）

3. <font style="color:#DF2A3F;">指令</font>

内置指令（vue本身自带的指令）和自定义指令（用户自己定义的指令）

4. <font style="color:#DF2A3F;">插件</font>

常用插件有：<font style="color:#ED740C;">Vue Router</font>（路由）、<font style="color:#ED740C;">Vuex</font>（状态管理库）、<font style="color:#ED740C;">Pinia</font>（轻量级状态管理库）

### Vue开发环境
（1）VS code[官网](https://code.visualstudio.com/)

（2）Node.js[官网](https://nodejs.org/zh-cn)

（win+R输入cmd，输入`node-v`，查看当前安装的Node版本）

（3）常见包管理器（npm和yarn）

需要各种第三方包来拓展项目功能，包是将一系列模板化的代码打包形成的。项目中所用到的包称为<font style="color:#ED740C;">项目的依赖</font>

<font style="color:#DF2A3F;">安装Node.js会自动安装相应版本的npm</font>

`npm-v`可以查看npm版本

安装yarn:`npm install yarn -g`

`yarn -v`查看yarn版本信息

#### 创建Vue项目
使用Vue3开发大型项目时，需要考虑目录结构、热加载、部署、代码单元测试等环节，使用Vite快速创建一个可以按需添加各种功能的项目

#### vite的简介
Vite是一个轻量级、运行速度快的前端构建工具，支持模块热替换，可以即时、准确地更新模块

#### 创建Vue3项目
（1）使用npm创建项目

`npm create vite@latest <项目名称> -- --template <模版名称>`

打开命令提示符，切换指定目录，使用npm创建一个基于Vite+Vue模版

`npm create vite@latest ahead-demo-01 -- --template vue`

切换到项目目录

`cd ahead-demo-01`

安装项目依赖

`npm install`

启动开发服务器

`npm run dev`

（2）使用yarn创建项目

`<font style="color:#DF2A3F;">yarn create vite <项目名称> --template vue</font>`

打开命令提示符，切换指定目录，使用yarn创建模版

`yarn create vite <项目名称> --template vue`

`cd <项目名称>`

`yarn`

`yarn dev` 

#### Vue3的结构目录
![](https://cdn.nlark.com/yuque/0/2025/png/56055817/1746857863989-24b3276d-5a4d-429e-a475-5401a5002798.png)

+ <font style="color:rgb(24, 30, 51);">vscode：存放VS Code编辑器的</font><font style="color:#DF2A3F;">相关配置文件</font><font style="color:rgb(24, 30, 51);">。</font>
+ <font style="color:rgb(24, 30, 51);">node_modules：存放项目的各种</font><font style="color:#DF2A3F;">依赖</font><font style="color:rgb(24, 30, 51);">和安装的</font><font style="color:#DF2A3F;">插件</font><font style="color:rgb(24, 30, 51);">。</font>
+ <font style="color:rgb(24, 30, 51);">public：存放</font><font style="color:#DF2A3F;">不可编译的静态资源文件</font><font style="color:rgb(24, 30, 51);">（</font><font style="color:rgba(0, 0, 0, 0.85);">favicon、robots.txt、sitemap.xml </font><font style="color:rgb(24, 30, 51);">），当进行项目构建时，该目录下的文件会被复制到dist目录，该目录下的文件需要使用</font><font style="color:#DF2A3F;">绝对路径访问</font><font style="color:rgb(24, 30, 51);">。（不需要被Webpack处理时，才考虑使用public文件夹）</font>
+ **<font style="color:rgb(24, 30, 51);">src：</font>**<font style="color:rgb(24, 30, 51);">源代码目录，保存开发人员编写的</font><font style="color:#DF2A3F;">项目源代码</font><font style="color:rgb(24, 30, 51);">。</font>
+ <font style="color:rgb(24, 30, 51);">·src\assets：存放</font><font style="color:#DF2A3F;">可编译的静态资源文件</font><font style="color:rgb(24, 30, 51);">，例如字体、图片、样式、CSS样式文件等。该目录下的文件需要使用</font><font style="color:#DF2A3F;">相对路径访问</font><font style="color:#000000;">或</font><font style="color:#DF2A3F;">模块引入</font><font style="color:rgb(24, 30, 51);">。</font>
+ ![](https://cdn.nlark.com/yuque/0/2025/png/56055817/1746858346331-7a8d772b-0318-4140-8a6b-4f6c4a4776a8.png)
+ **<font style="color:rgb(24, 30, 51);">src\components：</font>**<font style="color:rgb(24, 30, 51);">存放单文件组件，即.vue文件。（一般存放</font><font style="color:#DF2A3F;">可复用的子组件||功能组件</font><font style="color:rgb(24, 30, 51);">）功能积木，</font><font style="color:rgba(0, 0, 0, 0.85);">负责实现具体交互逻辑。</font>
+ <font style="color:rgb(24, 30, 51);">src＼App.vue：项目的</font><font style="color:#DF2A3F;">根组件</font><font style="color:rgb(24, 30, 51);">，项目启动时会被</font><font style="color:#DF2A3F;">首先加载</font><font style="color:rgb(24, 30, 51);">。（最定层的父组件）</font>
+ <font style="color:rgb(24, 30, 51);">Views：主要存放</font><font style="color:#DF2A3F;">页面级组件</font>（页面骨架，负责页面的UI结构，交互逻辑和整体布局）
+ <font style="color:rgb(24, 30, 51);">src＼main.js：项目的</font><font style="color:#DF2A3F;">入口文件</font><font style="color:rgb(24, 30, 51);">，决定页面渲染什么东西，用于创建Vue应用实例。引入对应组件框架一般需要配置相关实例</font>
+ <font style="color:rgb(24, 30, 51);">src＼style.css：项目的</font><font style="color:#DF2A3F;">全局样式</font><font style="color:rgb(24, 30, 51);">表文件。</font>
+ <font style="color:rgb(24, 30, 51);">.gitignore</font><font style="color:rgb(24, 30, 51);">：向</font><font style="color:rgb(24, 30, 51);">Git</font><font style="color:rgb(24, 30, 51);">仓库上传代码时需要忽略的文件列表。</font>
+ <font style="color:rgb(24, 30, 51);">index.html</font><font style="color:rgb(24, 30, 51);">：默认的主渲染页面文件，同时也是页面的入口文件。</font>
+ <font style="color:rgb(24, 30, 51);">package.json：包配置文件（项目名、版本号、依赖包、版本）。</font>
+ <font style="color:rgb(24, 30, 51);">README.md</font><font style="color:rgb(24, 30, 51);">：项目使用说明文件。</font>
+ <font style="color:rgb(24, 30, 51);">vite.config.js：存放Vite的相关配置(代理、</font><font style="color:#DF2A3F;">端口号</font><font style="color:rgb(24, 30, 51);">等)。</font>
+ <font style="color:rgb(24, 30, 51);">yarn.lock：存储每一个依赖项的安装版本，在使用yarn安装、升级、卸载依赖时，会自动更新yarn.lock文件。</font>

开发框架：

ElementPlus：

使用方法：[https://www.bilibili.com/video/BV1yGydYEE3H?spm_id_from=333.788.videopod.episodes&vd_source=752f03488469fc22671fa84a0c4f4304&p=156](https://www.bilibili.com/video/BV1yGydYEE3H?spm_id_from=333.788.videopod.episodes&vd_source=752f03488469fc22671fa84a0c4f4304&p=156)

### 一、数据绑定
1.setup语法糖（任何数据绑定都需要这个）

```javascript
<script setup>
  const 数据名=数据值
  </script>
```

2.输出数据（给定数据是包含HTML标签的字符串吗，会当成纯文本输出）

```javascript
<template>
  {{数据名}}
  </template>

```

### 二、响应式数据绑定
1. ref( )---用于数据

`const 数据名=ref(数据值)`

2. reactive( )---用于对象或数组

`const 数组名或对象名=reactive(对象或数组)`

3. toRef( )---对象中的单个属性

<font style="color:rgb(24, 30, 51);background-color:rgb(242, 242, 242);">const 对象名＝toRef（响应式对象，＇属性名＇）</font>

4. toRefs( )---对象中所有属性

<font style="color:rgb(24, 30, 51);background-color:rgb(242, 242, 242);">所有属性组成的对象＝toRefs（响应式对象）</font>

在script标签中需要修改响应式数据的值，要加`<font style="color:#DF2A3F;">.value</font>`进行修改

`数据名.value=新值`









## Vue Router
路由：路由器从一个接口收到数据，根据数据的目的地址将数据定向床送到另一个接口的行为和动作

路由器是执行行为和动作的硬件设备，主要用于网络连接，实现不同网络之间的通信和数据传递

#### <font style="color:rgb(19, 27, 38);">一、</font>**<font style="color:rgb(19, 27, 38);">Vue Router的安装</font>**
<font style="color:rgb(24, 30, 51);background-color:rgb(242, 242, 242);">yarn add vue-router@4 --save</font>

<font style="color:rgb(24, 30, 51);background-color:rgb(242, 242, 242);">yarn add: </font>用于安装心得依赖包到项目中

<font style="color:rgb(24, 30, 51);background-color:rgb(242, 242, 242);">vue-router@4:</font>指定安装的包名及版本号，@4表示安装vue router的第4个主板本

<font style="color:rgb(24, 30, 51);background-color:rgb(242, 242, 242);">--save:</font>标记将依赖添加到项目的package.json文件中（yarn默认行为，<font style="color:#DF2A3F;">可省略</font>）

查看版本号：在package.json文件中

#### <font style="color:rgb(19, 27, 38);">二、</font>**<font style="color:rgb(19, 27, 38);">Vue Router的基本使用</font>**
（1）创建路由配置

<font style="color:rgba(0, 0, 0, 0.85);">在 </font>`<font style="color:rgba(0, 0, 0, 0.85);">src/router/index.js</font>`<font style="color:rgba(0, 0, 0, 0.85);"> 中定义路由：（模版）</font>

```javascript
import { createRouter, createWebHistory } from 'vue-router';
import Home from '../views/Home.vue';//直接导入组件
import About from '../views/About.vue';

const router = createRouter({
  history: createWebHistory(),  // 指定路由的历史模式
  routes:[//路由配置数组，用来定义路径和组件之间的映射关系
    path: '/Home',          // 浏览器中显示的路径
    name: 'Home',       // 路由名称（可选）在导航守卫中的to.name中要使用到，
    //如果没有添加路由名称，就无法进行判断
    component: Home     // 该路由对应的Vue组件
  },
  {
    path: '/about',
    name: 'About',
    component: () => import('../views/About.vue')  // 懒加载方式挂载组件，
    //只有用户实际访问该路由时才会加载对应的组件代码
  }
]
});
export default router;
```

（2）在Vue应用中注册路由

<font style="color:rgba(0, 0, 0, 0.85);">在 </font>`<font style="color:rgba(0, 0, 0, 0.85);">main.js</font>`<font style="color:rgba(0, 0, 0, 0.85);"> 中引入并使用路由：</font>

```javascript
import { createApp } from 'vue';
import App from './App.vue';
import router from './router';  // 引入路由配置

const app = createApp(App);
app.use(router);  // 注册路由插件
app.mount('#app');
```

（3）在模版中<font style="color:#DF2A3F;">使用路由</font>

<font style="color:rgba(0, 0, 0, 0.85);">使用 </font>`<font style="color:rgba(0, 0, 0, 0.85);">router-link</font>`<font style="color:rgba(0, 0, 0, 0.85);"> 组件实现导航：</font>

<font style="color:rgba(0, 0, 0, 0.85);">在 </font>`<font style="color:rgba(0, 0, 0, 0.85);">App.vue</font>`<font style="color:rgba(0, 0, 0, 0.85);"> 中定义路由渲染位置：</font>

```vue
<template>
  <div>
    <router-link to="/home">首页</router-link>//to属性跳转到指定目标地址，是在对应router配置下的name值
    <router-view ></router-view> // 路由组件将渲染在这里
  </div>
</template>
```

<font style="color:rgba(0, 0, 0, 0.85);">当 </font>`<font style="color:rgba(0, 0, 0, 0.85);"><router-view></font>`<font style="color:rgba(0, 0, 0, 0.85);"> 不需要包裹任何内容时，使用单标签</font>`**<router-view />**`**也是Vue3写法**

<font style="color:rgba(0, 0, 0, 0.85);">当需要在 </font>`<font style="color:rgba(0, 0, 0, 0.85);"><router-view></font>`<font style="color:rgba(0, 0, 0, 0.85);"> 内部添加默认内容（如加载状态、过渡动画）时，必须使用双标签</font>

<font style="color:rgba(0, 0, 0, 0.85);">在Vue3中的变化</font>

+ 对于没有子节点的组件，推荐使用自闭合标签 `<router-view />`。
+ 对于有子节点的组件，必须使用双标签 `<router-view>...</router-view>`。

<font style="color:rgb(24, 30, 51);">在＜router-link＞标签中使用命名路由时，需要</font><font style="color:#DF2A3F;">动态绑定 to 属性的值</font><font style="color:rgb(24, 30, 51);">为对象.当使用对象作为to属性的值时，</font><font style="color:#DF2A3F;">to前面要加一个冒号</font><font style="color:rgb(24, 30, 51);">，表示使用v-bind指令进行绑定。在对象中，通过name属性指定要跳转到的路由名称，</font><font style="color:#DF2A3F;">使用params属性指定跳转时携带的路由参数</font><font style="color:rgb(24, 30, 51);">，语法格式如下。</font>

<font style="color:rgb(24, 30, 51);background-color:rgb(242, 242, 242);"><router-link :to="{name：路由名称，params：（参数名：参数值｝</router-link></font>

### 命名路由
使用name属性为路由匹配规则定义路由名称，即可实现命名路由（<font style="color:#DF2A3F;">name属性值不能重复，必须保证是唯一的</font>）

<font style="color:rgb(24, 30, 51);background-color:rgb(242, 242, 242);">｛path：’路由路径’,name：’路由名称’,component：组件｝</font>

<font style="color:rgb(24, 30, 51);background-color:rgb(242, 242, 242);"></font>

### 路由重定向（访问不同路径，页面显示同一个组件）
关键字 ：**redirect**

```javascript
const router=[{path:'/',redirect:'/home'}]  // 把路径重定向到/home
const router=[{path:'/',redirect:{name:'home'}}] //利用命名路由进行重定向
//动态重定向（使用beforeEnter守卫）
const routes = [
  {path: '/old-path',
    beforeEnter: (to, from, next) => {
      if (someCondition) {// 进行条件判断
        next('/new-path') // 满足条件时重定向到 /new-path
      } else {
        next('/another-path') // 不满足条件时重定向到 /another-path
      }}},]
//嵌套路由重定向（在子路由配置中使用redirect）
const routes = [{path: '/parent',component: ParentComponent,
    children: [{path: '', // 匹配 /parent
        redirect: 'child' // 重定向到子路由 /parent/child
          },]
//带参数的重定向
const routes = [
  {path: '/user/:id',redirect: to => {
      // 该函数会接收目标路由作为参数// 然后返回重定向的路径或命名路由
      return { name: 'profile', params: { id: to.params.id } }}},
  {path: '/profile/:id',name: 'profile',component: Profile}]
   
```

### 嵌套路由
在父路由配置中添加children数组来定义，子路由的路径会追加到父路径的后面

```javascript
// router/index.js
const routes = [
  {
    path: '/dashboard',
    component: () => import('../views/Dashboard.vue'),
    children: [
      // 默认子路由（访问 /dashboard 时显示）
      {
        path: '', // 空路径表示默认子路由，当用户访问父路由时自动渲染
        name: 'DashboardHome',
        component: () => import('../views/DashboardHome.vue')
      },
      // 子路由：/dashboard/settings
      {
        path: 'settings', // 注意：子路由不要以斜杠开头，否则会被视为根路径，不会继承父路由的路径
        name: 'DashboardSettings',
        component: () => import('../views/DashboardSettings.vue')
      },
    ]
  }
];
```

### 动态路由
(1)定义动态路由参数

<font style="color:rgba(0, 0, 0, 0.85);">在路由配置中，使用冒号 (</font>`<font style="color:rgba(0, 0, 0, 0.85);">:</font>`<font style="color:rgba(0, 0, 0, 0.85);">) 定义动态路径参数：</font>

```javascript
const routes = [
  {path: '/user/:id', // :id 是动态参数
  name: 'User',component: () => import('../views/User.vue')
  },
  {path: '/post/:category/:id', // 多个动态参数
  component: () => import('../views/Post.vue')
  }
];
```

(2)不同动态路径参数的动态路由在进行，切换时，因为它们都是指向统一组件，所以vue<font style="color:#DF2A3F;">不会销毁再重新创建这个组件</font>，，这意味着<font style="color:#DF2A3F;">组件的生命周期钩子不会再次出发</font>，如果想要在切换时进行一些操作，就需要在组件内部利用<font style="color:#DF2A3F;">watch来监听路由的变化or使用onBeforeRouteUpdate导航守卫</font>

(3)在组件中获取参数（$route.params.id访问动态参数）

```javascript
<template>
  <div>
    <h1>用户ID: {{ userId }}</h1>
    <p>文章分类: {{ $route.params.category }}</p>
  </div>
</template>
<script setup>
import { useRoute } from 'vue-router';
const route = useRoute();
const userId = route.params.id; // 获取参数
```

### 


### 路由进阶
#### 一、编程式导航
<font style="color:rgb(0, 0, 255);">先通过useRouter()函数获取全局路由实例，然后通过调用全局路由实例实现导航</font><font style="color:rgb(24, 30, 51);">。</font>

<font style="color:rgb(24, 30, 51);">（1）导包、创建全局路由</font>

```plain
import { useRouter } from 'vue-router'
const router = useRouter()
```

（2）push（）方法：<font style="color:rgba(0, 0, 0, 0.85);">用于导航至新路由，会向历史记录添加一条新记录，以编程方式导航到一个新的URL</font>

```javascript
// 字符串路径形式
router.push('/home')
// 对象形式
router.push({ path: '/home' })
// 带查询参数的情况
router.push({ name: 'user', params: { userId: '123' }, query: { key: 'value' } })
// 带hash值的情况
router.push({ path: '/home', hash: '#top' })
//如果在参数的对象中提供了path，则params会被忽略
router.push({ path: '/user', params: { userId}})
```

（3）replace（）方法：<font style="color:rgb(24, 30, 51);">和push（）类似，但在导航后不会向历史记录中添加新的记录，而是会替换历史记录中的当前记录。</font>

```javascript
//编程式导航
router.replace({ path: '/user' })
＜！-- 声明式导航 --＞
<router-link:to="(path: '/user' }" replace></router-link>//改成push则为push（）
```

  
（4）go（）方法：<font style="color:rgb(24, 30, 51);">用于实现前进或后退的效果，其参数表示历史记录中前进或后退的步数</font>

```javascript
// 后退一步，等同于 router.back()
router.go(-1)

// 前进一步，等同于 router.forward()
router.go(1)
```

注意

<font style="color:#DF2A3F;background-color:rgba(0, 0, 0, 0.04);">router.push('/home')和router.push('home')的区别是什么？</font>

<font style="color:#2F4BDA;background-color:rgba(0, 0, 0, 0.04);">绝对路径和相对路径的使用</font>

| **写法** | **路径类型** | **解析规则** | **示例（当前路由为**** **`**/main**`<br/>** ****时）** |
| :--- | :--- | :--- | :--- |
| `router.push('/home')` | 绝对路径 | 从根路径开始解析 | 跳转至 `/home` |
| `router.push('home')` | 相对路径 | 相对于当前路由解析 | 跳转至 `/main/home` |


#### 二、导航守卫
（1）<font style="color:rgb(24, 30, 51);">全局导航守卫</font>

<font style="color:rgb(24, 30, 51);">全局前置守卫beforeEach()和全局后置守卫afterEach()</font>

```javascript
const router = createRouter()
router.beforeEach((to,from,next)⇒(相关操作)
router.afterEach((to, from,next)⇒(相关操作)
```

to：表示目标路由对象

from：表示 当前导航正要离开的路由

next为函数，<font style="color:rgb(24, 30, 51);">如果不接收 next()函数，则默认允许用户访问每一个路由；如果接收了next（）函数，则必须调用next（）函数，否则不允许用户访问任何一个路由。</font>

+ 导航守卫可以直接返回以下值：
    - `undefined` 或 `true`：允许导航（等同于 `next()`）
    - `false`：取消导航（等同于 `next(false)`）
    - 路由地址（字符串或对象）：重定向（等同于 `next('/path')`）
    - `Error` 对象：触发全局错误处理

```javascript
// Vue Router 3.x（使用 next）
router.beforeEach((to, from, next) => {
  if (isAuthenticated()) {
    next()
  } else {
    next('/login')
  }
})

// Vue Router 4.x（直接返回）
router.beforeEach((to, from) => {
  if (isAuthenticated()) {
    return true // 或省略 return（默认允许）
  } else {
    return '/login' // 重定向
  }
})
```

<font style="color:rgb(24, 30, 51);">（2）导航独享守卫</font>

<font style="color:rgb(24, 30, 51);">目前只有beforeEnter()守卫，只有在路由导航到一个不同的页面时才会被触发，beforeEnter()守卫只适用于单个路由。</font>

<font style="color:rgb(24, 30, 51);">（3）组件导航守卫</font>

<font style="color:rgb(24, 30, 51);">beforeRouteEnter()守卫在路由进入之前被触发；beforeRouteUpdate()守卫在路由更新之前被触发；beforeRouteLeave()守卫在路由离开之前被触发。</font>

## <font style="color:rgb(24, 30, 51);">状态管理和网络请求</font>
### Axios
基于Promise的HTTP客户端，可以发送get、post等请求，作用于浏览器和Node.js中

#### json-server
安装

在对应文件夹下输入cmd

`npm install -g json-server`

创建db.json文件

```javascript
{
  "posts": [
    { "id": "1", "title": "a title", "views": 100 },
    { "id": "2", "title": "another title", "views": 200 }
  ],
  "comments": [
    { "id": "1", "text": "a comment about post 1", "postId": "1" },
    { "id": "2", "text": "another comment about post 1", "postId": "1" }
  ],
  "profile": {
    "name": "typicode"
  }
}
```

启动服务

npx json-server db.json

json-server --watch db.json

#### 安装Axios
（1）标签引入

<font style="color:rgb(24, 30, 51);">①</font><font style="color:rgb(24, 30, 51);">使用</font><font style="color:rgb(24, 30, 51);">Unpkg</font><font style="color:rgb(24, 30, 51);">的</font><font style="color:rgb(24, 30, 51);">CDN</font><font style="color:rgb(24, 30, 51);">服务引入</font><font style="color:rgb(24, 30, 51);">Axios</font><font style="color:rgb(24, 30, 51);">的示例代码如下。</font>

<font style="color:rgb(24, 30, 51);background-color:rgb(242, 242, 242);"><scriptsrc="https://unpkg.com/axios/dist/axios.min.js"></script></font>

<font style="color:rgb(24, 30, 51);">②</font><font style="color:rgb(24, 30, 51);">使用</font><font style="color:rgb(24, 30, 51);">jsDelivr</font><font style="color:rgb(24, 30, 51);">的</font><font style="color:rgb(24, 30, 51);">CDN</font><font style="color:rgb(24, 30, 51);">服务引入</font><font style="color:rgb(24, 30, 51);">Axios</font><font style="color:rgb(24, 30, 51);">的示例代码如下。</font>

<font style="color:rgb(24, 30, 51);background-color:rgb(242, 242, 242);"><scripttps://cdn.jsdelivr.net/npm/axios/dist/axios.min.js"></script></font>

（2）使用包管理器工具安装

<font style="color:rgb(24, 30, 51);">＃</font><font style="color:rgb(24, 30, 51);">使用</font><font style="color:rgb(24, 30, 51);">npm</font><font style="color:rgb(24, 30, 51);">包管理工具安装</font>

<font style="color:rgb(24, 30, 51);background-color:rgb(242, 242, 242);">npm install axios --save</font>

<font style="color:rgb(24, 30, 51);">＃</font><font style="color:rgb(24, 30, 51);">使用</font><font style="color:rgb(24, 30, 51);">yarn</font><font style="color:rgb(24, 30, 51);">包管理工具安装</font>

<font style="color:rgb(24, 30, 51);background-color:rgb(242, 242, 242);">yarn add axios --save</font>

<font style="color:rgb(24, 30, 51);">项目启动后，会默认开启一个本地服务，地址为http://127.0.0.1:5173/。</font>

#### <font style="color:rgb(24, 30, 51);">Axios请求响应体结果（console.log(Response)）</font>
<font style="color:rgb(24, 30, 51);">config:配置对象</font>

<font style="color:rgb(24, 30, 51);">data：响应体结果</font>

<font style="color:rgb(24, 30, 51);">headers：响应头信息</font>

<font style="color:rgb(24, 30, 51);">request：原生AJAX请求对象</font>

<font style="color:rgb(24, 30, 51);">status：响应状态码</font>

<font style="color:rgb(24, 30, 51);">statusText：响应状态字符串</font>

#### <font style="color:rgb(24, 30, 51);">默认配置</font>
<font style="color:rgb(24, 30, 51);"></font>

#### 使用Axios
（1）在scr目录下创建axios文件夹，再在下面创建request.js文件

```javascript
// 封装axios请求库
import axios from "axios";
//创建实例对象
const request = axios.create({
    timeout: 2000//设置超时时间为2秒
});
export default request;
```

### Vuex
### <font style="color:rgb(24, 30, 51);">Pinia（比Vuex更好用）</font>
<font style="color:rgb(24, 30, 51);">新一代的轻量级状态管理库，它允许跨组件或页面共享状态，解决多组件的数据通信问题</font>

<font style="color:rgb(24, 30, 51);">（1）安装</font>

<font style="color:rgb(24, 30, 51);background-color:rgb(242, 242, 242);">yarn：yarn add pinia --save</font>

<font style="color:rgb(24, 30, 51);background-color:rgb(242, 242, 242);">npm：npm install pinia --save</font>

（2）创建Store模块

1. 在src文件夹下创建store文件夹，创建index.js 文件
2. 在index.js中引入createPinia函数

```javascript
import { definestore} from 'pinia'//从pinia中导入defineStore函数，该方法用于创建store对象
export const useStore = defineStore('storeId',{//用于在组件中获取store对实例，useStore是
  //随机定义的，在APP.vue中需要导入这个函数（但是在pinia的规范中，一般以use开头来命名）
  //第一个参数是store的唯一标识符，用来区分和管理不同的store
  state:()⇒{//定义数据，用return{变量名：变量值}返回一个变量名：变量值:函数式
  
  },//用于管理数据
  getters:{//对象式。计算属性，用于获取数据
    
  },
  actions:{//对象式。定义事件处理方法，进行同步或异步操作
    
  }
})
```

3. 在main.js文件中引入store文件夹中的index.js文件，并将其挂载到Vue实例上

```javascript
import { createApp } from 'vue'
import './style.css'
import { createPinia } from 'pinia'//导入pinia
const app=createApp(App)//创建vue实例
const pinia=createPinia()//创建pinia实例
app.use(pinia)//将pinia实例挂载到vue实例上
app.mount('#app')
```

4. 在组件中导入并使用



```vue
import { storeToRefs } from 'pinia';
  import { useStore } from './store';//如果store文件夹下有index.js则为'./store'，如果命名为其他则需要写完整路径
  const store=useStore();
const{add,reduce}=storeToRefs(store)//对属性进行响应式处理，将index.js中state定义的变量拿给组件使用，getters方法中的方法返回值的使用与state的变量使用方法一致
```



<font style="color:rgb(24, 30, 51);">getter中有只读特性，组件中使用getters和state方法类似</font>

相关要点：

1.在vue组件运行时需要一个实际的DOM节点来挂载，因此：即使在template中没有div，Vue也会自动创建一个默认的根div元素

2.使用scoped样式可以确保样式只应用到本组件元素中

3.@是Vue CLI默认配置的别名，指向src目录

4.图片需要动态变化时，可在JavaScript中导入图片再通过:src 绑定

5.JavaScript的暂时性死区问题，在router.js文件里，当你导入Login组件，可能因为代码顺序或模块加载问题，使用Login组件之前它还没有被正确初始化。解决方案是采用动态导入方式来加载组件，保证在需要使用该组件时再去加载

6.使用ElementPlus图标需要在main.js中导入`import * as ElementPlusIconsVue from '@element-plus/icons-vue'`，同时还要全局注册ElementPlus图标

```javascript
for (const [key, component] of Object.entries(ElementPlusIconsVue)) {
    app.component(key, component)//全局注册ElementPlus图标
}
```

注册ElementPlus，设置大小`app.use(ElementPlus, {size: setting.theme.size})`


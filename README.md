# vue

## 项目结构：

```bash
src
├── compiler        # 编译相关 
├── core            # 核心代码 
├── platforms       # 不同平台的支持
├── server          # 服务端渲染
├── sfc             # .vue 文件解析
├── shared          # 共享代码
```

## vue对象

在使用 `vue` 时我们都是使用 `new Vue()` ,来将 `vue` 的实例挂载到 `dom` 对象上从而运用数据驱动的方式来扩展我们的代码，`vue` 项目中 `main.js`

```javascript
import Vue from "vue";
import App from "./App.vue";
import router from "./router";
import store from "./store";

Vue.config.productionTip = false;

new Vue({
  router,
  store,
  render: h => h(App)
}).$mount("#app");
```

从源头上看来自 `core` 目录下的 `instance` 的 `index.js` 文件
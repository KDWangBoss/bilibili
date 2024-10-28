```
// chrome的一款可以查看vue2生产环境组件状态的插件
Vue force dev


投产环境开启 vue-devtools，打开控制台,运行一下以下代码：var Vue, walker, node;walker = document.createTreeWalker(document.body,1);while ((node = walker.nextNode())) {  if (node.__vue__) {    Vue = node.__vue__.$options._base;    if (!Vue.config.devtools) {      Vue.config.devtools = true;      if (window.__VUE_DEVTOOLS_GLOBAL_HOOK__) {        window.__VUE_DEVTOOLS_GLOBAL_HOOK__.emit("init", Vue);        console.log("==> vue devtools now is enabled");      }    }    break;  }}
```


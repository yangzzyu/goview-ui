<!--
 * @Author: yangyu 1431330771@qq.com
 * @Date: 2021-12-11 19:46:50
 * @LastEditors: yangyu 1431330771@qq.com
 * @LastEditTime: 2024-12-30 17:54:22
 * @FilePath: \goview-ui-main\README.md
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->

> 基于GoView低代码平台的可视化ui组件

![IMG_5885](https://yangzzyu.github.io/goview-ui/assets/1734597091546.jpg)

该组件需要配合 GoView 使用，在 GoView 低代码平台拖拽并配置完成后，下载导出对应页面的 json 数据格式，再传该组件进行展示。

## npm/pnpm 方式安装使用

```shell
npm i goview-ui
pnpm i goview-ui
```

### 全局注册使用

```js
// 在main.js中按下引入
import goViewui from "goview-ui";
import "goview-ui/dist/style.css";
import { createPinia } from "pinia";
const pinia = createPinia();
const app = createApp(App);
window["$vue"] = app;
window["pinia"] = pinia;
app.use(pinia).use(goViewui).mount("#app");
```

![image](https://yangzzyu.github.io/goview-ui/assets/b217be17d8d98e0197876f39171c8ed.png)

## 使用插槽自定义内容

在 GoView 平台组件无法满足项目业务需求时，可使用插槽对区域内容进行自定义。

```js

 <goView :dataJson="dataJson">
    <template #map>
      <div style="background: red;width: 100%;height: 100%;">
        <h1 style="color: #fff;">地图</h1>
      </div>
      <template #id_4fx2fk7cqzk000>
        <div style="background: red; width: 100%; height: 100%">
          <h1 style="color: #fff">通过id进行插槽定义</h1>
        </div>
      </template>
    </template>
  </goView>
```
定义插槽名称
![image](https://yangzzyu.github.io/goview-ui/assets/99cb469c2e74ac6d2b3e59f9bc03357.png)


代码示例
<!-- ![image](https://yangzzyu.github.io/goview-ui/assets/1734673662701.jpg) -->
![image](https://yangzzyu.github.io/goview-ui/assets/1735551220706.jpg)

[GoView 在线体验
](https://vue.mtruning.club/)

[goview-ui Github 在线文档示例
](https://yangzzyu.github.io/goview-ui)

### 交流/打赏

![image](https://yangzzyu.github.io/goview-ui/assets/1734597998336.jpg)

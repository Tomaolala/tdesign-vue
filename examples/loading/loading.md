## Loading 加载 

::: demo demos/base 默认
:::

::: demo demos/size 大小
:::

::: demo demos/indicatorSlot slot 加载符
:::

::: demo demos/indicatorFunc function 加载符
:::

::: demo demos/text 文字加载
:::

::: demo demos/wrap 有包裹
:::

::: demo demos/delay 有延时
:::

::: demo demos/fullscreen 全屏加载
:::


::: demo demos/service 函数方式调用
:::

### 属性配置
| 属性 | 类型 | 默认值 | 必传 | 说明 |
|-----|-----|-----|-----|-----|
|indicator|TNode|圆圈图标|N|加载指示符（支持function、slot。不支持string）|
|text|TNode|无|N|自定义的加载提示文案|
|loading|boolean|false|Y|是否为加载中状态|
|size|string|medium|N|加载组件大小，包括图标和文字。可选值为 large/medium/small|
|delay|number(毫秒)|0|N|延迟显示加载效果的时间（防止闪烁）|
|fullscreen|boolean|false|N|是否全屏遮罩，遮罩会插入至 body 上。开启全屏加载时，loading必须作为包裹元素|
|preventScrollThrough|boolean|false|N|是否需要锁定屏幕的滚动|
|className|string|无|N|包裹器的自定义类名|
|showOverlay|boolean|true|N|是否需要遮罩层，遮罩层对包裹元素才有效|

### Loading Plugin

该插件已默认引入组件库总包。如果项目要按需加载插件，则需要自行装载该插件，示例代码如下：

```js
import Vue from 'vue';
import { LoadingPlugin } from './loading';
const Plugin = {
  install: (Vue) => {
    Vue.prototype.$loading = LoadingPlugin;
  }
};
Vue.use(Plugin);
```

* 调用方式：this.$loading(options)
* options的参数同组件方式调用时的参数，但只支持全屏模式的加载，fullscreen为true，不可配置。

options可配置参数如下：

| 属性 | 类型 | 默认值 | 必传 | 说明 |
|-----|-----|-----|-----|-----|
|indicator|TNode|圆圈图标|N|加载指示符（支持function、slot。不支持string）|
|text|TNode|无|N|自定义的加载提示文案|
|loading|boolean|false|Y|是否为加载中状态|
|size|string|medium|N|加载组件大小，包括图标和文字。可选值为 large/medium/small|
|delay|number(毫秒)|0|N|延迟显示加载效果的时间（防止闪烁）|
|preventScrollThrough|boolean|false|N|是否需要锁定屏幕的滚动|
|className|string|无|N|包裹器的自定义类名|
|showOverlay|boolean|true|N|是否需要遮罩层，遮罩层对包裹元素才有效|


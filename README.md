# vue2-index-list

> it is a usefull index-list component based on vue2.x<br/>基于vue2.x实现的一个类似通讯录的展示组件，带索引高亮联动效果，使用时请看下注意事项

# 立即使用（How to use)
> 引入src/components/index-list.vue组件
```html
<template>
  <div class="wrap">
    <index-list :data="testData" v-if="testData.length"></index-list>
  </div>
</template>
<style lang="css">
  .wrap{
    position:fixed;
    top:0;
    bottom:0;
    width:100%;
  }
</style>
```
# 参数（Options）
```javascript
  props: {
    data: {
      type: Array,
      default: []
    }
  }
```
# 事件名
> choose：每个列表项可以绑定该事件，会传递一个参数（item）包含当前项的数据

# 注意事项（Attention）
* 包裹组件的父级元素必须设置fixed定位，这里滚动是原生的overflow:auto，样式控制需要使用者自己做些调整
* data的数据格式严格遵循根目录testData.json里面的格式，当然你也可以修改源码来实现自己的格式

# 演示效果
<img src="http://cdn.zhangxuefei.site/wp-content/uploads/2017/08/vue2-index-list.gif">

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
    },
    useLazyLoad: { //如果开启需要依赖vue-lazyload组件
      type: Boolean,
      default: false
    }
  }
```
# 事件名
> choose：点击每项时触发，会传递一个参数（item）包含当前项的数据

# 注意事项（Attention）
* 包裹组件的父级元素必须设置fixed定位，这里滚动是原生的overflow:auto，样式控制需要使用者自己做些调整
* data的数据格式严格遵循根目录testData.json里面的格式，当然你也可以修改源码来实现自己的格式

# 模块依赖（Dependencies）
> 涉及到多张图片加载，建议引入组件vue-lazyload，并且设置useLazyLoad:true

# 演示效果
![预览地址](http://cdn.zhangxuefei.site/wp-content/uploads/2017/08/vue2-index-list.gif)

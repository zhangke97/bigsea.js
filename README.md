# bigsea.js

源码 https://github.com/BIGC-HUB/bigsea.js/blob/master/bigsea.js

示例

DOM 操作同 jQuery

#### 事件监听

```js
Sea('body').on('click', function () {
  log('点击 body')
})
```

#### 事件委托

```js
Sea('body').on('click', '.user', function () {
  log('点击 body 中的 .user 元素')
})
```

#### 一次性事件

```js
Sea('body').one('click', function () {
  log('点击 body 后，自动销毁该监听')
})
```

#### 移除所有事件

```js
Sea('body').off()
```

#### [观察者模式](https://www.cnblogs.com/jscode/p/3600060.html)

```js
Sea('body').ob(
  {
    childList: true, // 子元素的变动
    attributes: true, // 属性的变动
    characterData: true, // 节点内容或节点文本的变动
    subtree: true, // 所有下属节点（包括子节点和子节点的子节点）的变动
    attributeOldValue: true, // 需要记录变动前的属性值
    characterDataOldValue: true, // 需要记录变动前的数据值
    attributesFilter: ['class', 'str'], // 值为一个数组，表示需要观察的特定属性
  },
  function (event) {
    log(event)
  },
)
```

联系作者 c@bigc.cc

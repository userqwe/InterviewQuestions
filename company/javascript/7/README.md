# （阿里巴巴）简述懒加载

懒加载也叫延迟加载，指的是在长网页中延迟加载图像，是一种很好优化网页性能的方式。

懒加载的优点：
  1. 提升用户体验，加快首屏渲染速度；
  2. 减少无效资源的加载；
  3. 防止并发加载的资源过多会阻塞 js 的加载；

懒加载的原理：

首先将页面上的图片的 `src` 属性设为空字符串，而图片的真实路径则设置在 `data-original` 属性中，当页面滚动的时候需要去监听 `scroll` 事件，在 `scroll` 事件的回调中，判断我们的懒加载的图片是否进入可视区域，如果图片在可视区内则将图片的 `src` 属性设置为 `data-original` 的值，这样就可以实现延迟加载。
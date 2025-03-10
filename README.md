### 1万行数据渲染
- 后端：使用math.random模拟生成10000条数据，并返回json数据。
- 前端：使用fetch 请求后端数据，并渲染到页面上。
- 性能优化：
  - 使用虚拟列表，只渲染可视区域内的数据。
  - 使用useCallback，避免每次渲染都重新创建函数。
- 体验优化：
  - 使用"加载中..."，提示用户数据正在加载。
  - 使用箭头滚动事件，超过100行，出现箭头返回页面顶端；当滚动到最底部时，加载更多数据。
- 考虑其他优化
  - 分页
  - 懒加载
  - 缓存数据
  - 防抖节流，减少请求次数

### 演示效果
![虚拟列表演示](./public/视频演示.gif)
# 《前端性能揭秘》

本仓库为《前端性能揭秘》的勘误仓库，欢迎有问题在 `issue` 区讨论，或通过 Pull Request 贡献，或者加入读者群。

![4371665910372_ pic](https://user-images.githubusercontent.com/5436704/196026960-4e56539d-5e7c-485e-8cb9-becd387c09c3.jpg)

## 购买链接

- [京东购买地址](https://item.jd.com/13387853.html)

## 贡献者

- TODO

## 勘误

- 207 页补充段落在 `小结` 前

需要注意的是，使用 ServiceWorker 并不代表能给性能带来直接的提升。事实上 ServiceWorker 之所以可以被用于改善性能，是因为 ServiceWorker 提供了更加灵活的缓存和预缓存策略，使得我们可以在一些 HTTP 缓存无法满足使用条件的场景使用缓存和预缓存的能力，从而带来性能的提升，而并非因为 ServiceWorker 本身。

事实上，单纯的引入 ServiceWorker 因为增加本身的网络请求、增加冷启动和使用逻辑反而会带来一些性能上的负担。所以在 HTTP 缓存能够满足需求的场景，引入 ServiceWorker 替代原有的 HTTP 缓存是没有必要的。


- 176 页，`宏任务` 描述不精确，在整个章节中都应该替换为 `任务`，同时补充以下内容


注：也有一些文章或书籍将任务（Task）称为宏任务（MacroTask）用于和微任务（MicroTask）区分，但事实上在 W3C 标准中只有任务和微任务，并没有宏任务这样的名称。


- 181 页，应该为 `涉及` 而不是 `设计`
- 181 页补充说明


虽然本节以 Promise Polyfill 为例讲解了采取任务和微任务对于性能的影响，但并非所有的 Promise Polyfill 的性能都存在问题，事实上只要采取正确的方式实现，例如在老版本浏览器中采用 Mutation Observer 模拟，Promise Polyfill 的性能并不会和浏览器原生的 Promise 实现存在明显差异。

# page

## state.pool

可以在多页 tab 模式下显示的页面

## state.opened

当前显示的多页面列表

## state.current

当前页面

## state.keepAlive

需要缓存的页面 name 数组

## mutations.keepAliveRefresh

### 介绍

从已经打开的页面记录中更新需要缓存的页面记录。

### 参数

无

### 示例

``` js
this.$store.commit('d2admin/page/keepAliveRefresh')
```

## mutations.keepAliveRemove

### 介绍

删除一个页面的缓存设置。

### 参数

| 参数名 | 介绍 | 必选 | 值类型 | 可选值 | 默认值 |
| --- | --- | --- | --- | --- | --- |
| name | route name | 必选 | String |  |  |

### 示例

``` js
this.$store.commit('d2admin/page/keepAliveRemove', 'page-name')
```

## mutations.keepAlivePush

### 介绍

增加一个页面的缓存设置。

### 参数

| 参数名 | 介绍 | 必选 | 值类型 | 可选值 | 默认值 |
| --- | --- | --- | --- | --- | --- |
| name | route name | 必选 | String |  |  |

### 示例

``` js
this.$store.commit('d2admin/page/keepAlivePush', 'page-name')
```

## mutations.keepAliveClean

### 介绍

清空页面缓存设置。

### 参数

无

### 示例

``` js
this.$store.commit('d2admin/page/keepAliveClean')
```

## mutations.open

### 介绍

打开一个新的页面。

### 参数

| 参数名 | 介绍 | 必选 | 值类型 | 可选值 | 默认值 |
| --- | --- | --- | --- | --- | --- |
| name | route name | 必选 | String |  |  |
| params | route params | 非 | Object |  |  |
| query | route query | 非 | Object |  |  |

### 示例

``` js
router.afterEach(to => {
  // 需要的信息
  const app = router.app
  const { name, params, query } = to
  // 多页控制 打开新的页面
  app.$store.commit('d2admin/page/open', { name, params, query })
})
```

## mutations.currentSet

### 介绍

设置当前激活的页面 name。

### 参数

| 参数名 | 介绍 | 必选 | 值类型 | 可选值 | 默认值 |
| --- | --- | --- | --- | --- | --- |
| name | route name | 必选 | String |  |  |

### 示例

``` js
this.$store.commit('d2admin/page/currentSet', 'route-name')
```

## mutations.openedUpdate

### 介绍

更新页面列表上的某一项。

### 参数

| 参数名 | 介绍 | 必选 | 值类型 | 可选值 | 默认值 |
| --- | --- | --- | --- | --- | --- |
| index | 已经打开的页面的位置 | 必选 | Number |  |  |
| params | route params | 非 | Object |  |  |
| query | route query | 非 | Object |  |  |

### 示例

``` js
this.$store.commit('d2admin/page/openedUpdate', {
  index: 2,
  params: {
    name: 'new-name'
  },
  query: {
    value: 'new-value'
  }
})
```

## mutations.opend2db

### 介绍

将 opened 属性赋值并持久化。

::: tip
在这之前请先确保已经更新了 state.opened。
:::

### 参数

无

### 示例

``` js
this.$store.commit('d2admin/page/opend2db')
```

## mutations.openedLoad

### 介绍

从持久化数据载入分页列表。

### 参数

无

### 示例

``` js
this.$store.commit('d2admin/page/openedLoad')
```

## mutations.add

### 介绍

新增一个 tag。

### 参数

| 参数名 | 介绍 | 必选 | 值类型 | 可选值 | 默认值 |
| --- | --- | --- | --- | --- | --- |
| tag | { name, path, meta } | state.pool 中的某项 | Object |  |  |
| params | route params | 非 | Object |  |  |
| query | route query | 非 | Object |  |  |

### 示例

``` js
this.$store.commit('d2admin/page/add', {
  tag: {
    name: 'route-name',
    path: 'route-path',
    meta: {}
  },
  params: {},
  query: {}
})
```

## mutations.close

### 介绍

关闭一个 tag。

### 参数

| 参数名 | 介绍 | 必选 | 值类型 | 可选值 | 默认值 |
| --- | --- | --- | --- | --- | --- |
| tagName | 要关闭的标签名字 | 必选 | String |  |  |
| vm | vue 实例 | 必选 | Object |  |  |

### 示例

``` js
this.$store.commit('d2admin/page/close', {
  tagName: 'route-name',
  vm: this
})
```

## mutations.closeLeft

### 介绍

关闭当前标签左边的标签。

### 参数

| 参数名 | 介绍 | 必选 | 值类型 | 可选值 | 默认值 |
| --- | --- | --- | --- | --- | --- |
| pageSelect | 当前选中的 tagName | 必选 | String |  |  |
| vm | vue 实例 | 必选 | Object |  |  |

### 示例

``` js
this.$store.commit('d2admin/page/closeLeft', {
  pageSelect: 'route-name',
  vm: this
})
```

## mutations.closeRight

### 介绍

关闭当前标签右边的标签。

### 参数

| 参数名 | 介绍 | 必选 | 值类型 | 可选值 | 默认值 |
| --- | --- | --- | --- | --- | --- |
| pageSelect | 当前选中的 tagName | 必选 | String |  |  |
| vm | vue 实例 | 必选 | Object |  |  |

### 示例

``` js
this.$store.commit('d2admin/page/closeRight', {
  pageSelect: 'route-name',
  vm: this
})
```

## mutations.closeOther

### 介绍

关闭当前激活之外的标签。

### 参数

| 参数名 | 介绍 | 必选 | 值类型 | 可选值 | 默认值 |
| --- | --- | --- | --- | --- | --- |
| pageSelect | 当前选中的 tagName | 必选 | String |  |  |
| vm | vue 实例 | 必选 | Object |  |  |

### 示例

``` js
this.$store.commit('d2admin/page/closeOther', {
  pageSelect: 'route-name',
  vm: this
})
```

## mutations.closeAll

### 介绍

关闭所有标签。

### 参数

| 参数名 | 介绍 | 必选 | 值类型 | 可选值 | 默认值 |
| --- | --- | --- | --- | --- | --- |
| vm | vue 实例 | 必选 | Object |  |  |

### 示例

``` js
this.$store.commit('d2admin/page/closeAll', {
  vm: this
})
```

## mutations.init

### 介绍

初始化多页面功能，将路由设置转化为 store 中的预备数据

### 参数

| 参数名 | 介绍 | 必选 | 值类型 | 可选值 | 默认值 |
| --- | --- | --- | --- | --- | --- |
| routes | 路由设置 | 必选 | Array |  |  |

### 示例

``` js
import { frameInRoutes } from '@/router/routes'
this.$store.commit('d2admin/page/init', frameInRoutes)
```
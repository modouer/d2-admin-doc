# fullscreen

## state.active

当前的全屏状态激活标识

## mutations.toggle

### 介绍

切换全屏。

### 参数

无

### 示例

``` js
this.$store.commit('d2admin/fullscreen/toggle')
```

## mutations.set

### 介绍

设置全屏状态。

### 参数

| 参数名 | 介绍 | 必选 | 值类型 | 可选值 | 默认值 |
| --- | --- | --- | --- | --- | --- |
| active | 新的值 | 必选 | Boolean |  |  |

### 示例

``` js
// 打开全屏
this.$store.commit('d2admin/fullscreen/set', true)
// 关闭全屏
this.$store.commit('d2admin/fullscreen/set', false)
```
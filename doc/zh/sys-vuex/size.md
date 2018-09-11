# size

## state.value

全局尺寸

## mutations.set

### 介绍

设置全局尺寸。

### 参数

| 参数名 | 介绍 | 必选 | 值类型 | 可选值 | 默认值 |
| --- | --- | --- | --- | --- | --- |
| size | 尺寸 | 必选 | String |  |  |

### 示例

``` js
this.$store.commit('d2admin/size/set', 'mini')
```

## mutations.load

### 介绍

从持久化数据读取尺寸设置。

### 参数

无

### 示例

``` js
this.$store.commit('d2admin/size/load')
```
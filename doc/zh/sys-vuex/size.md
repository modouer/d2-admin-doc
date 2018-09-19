# size

## state.value

全局尺寸

## actions.set

### 介绍

设置全局尺寸。

### 参数

| 参数名 | 介绍 | 必选 | 值类型 | 可选值 | 默认值 |
| --- | --- | --- | --- | --- | --- |
| size | 尺寸 | 必选 | String |  |  |

### 返回

promise

### 示例

``` js
this.$store.dispatch('d2admin/size/set', 'mini')
```

## actions.load

### 介绍

从持久化数据读取尺寸设置。

### 参数

无

### 返回

promise

### 示例

``` js
this.$store.dispatch('d2admin/size/load')
```
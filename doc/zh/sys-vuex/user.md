# user

## state.info

用户信息

## mutations.set

### 介绍

设置用户数据。

### 参数

| 参数名 | 介绍 | 必选 | 值类型 | 可选值 | 默认值 |
| --- | --- | --- | --- | --- | --- |
| info | 用户数据 | 必选 | Object |  |  |

### 示例

``` js
this.$store.commit('d2admin/user/set', {
  name: 'my-name'
})
```

## mutations.load

### 介绍

从持久化数据读取用户数据。

### 参数

无

### 示例

``` js
this.$store.commit('d2admin/user/load')
```
# releases

## state.version

当前版本

## state.latest

最新版本的信息

## state.update

有新版本

## actions.checkUpdate

### 介绍

检查版本更新。

### 参数

无

### 示例

``` js
this.$store.dispatch('d2admin/releases/checkUpdate')
```

## mutations.versionShow

### 介绍

显示版本信息。

### 参数

无

### 示例

``` js
this.$store.commit('d2admin/releases/versionShow')
```

## mutations.updateSet

### 介绍

设置是否有新的 D2Admin 版本。

### 参数

| 参数名 | 介绍 | 必选 | 值类型 | 可选值 | 默认值 |
| --- | --- | --- | --- | --- | --- |
| update | 是否有新版本 | 必选 | Boolean |  |  |

### 示例

``` js
this.$store.commit('d2admin/releases/updateSet', true)
```

## mutations.latestSet

### 介绍

设置最新版本的信息。

### 参数

| 参数名 | 介绍 | 必选 | 值类型 | 可选值 | 默认值 |
| --- | --- | --- | --- | --- | --- |
| latest | 最新版本的信息 | 必选 | Object |  |  |

### 示例

``` js
this.$store.commit('d2admin/releases/latestSet', {})
```
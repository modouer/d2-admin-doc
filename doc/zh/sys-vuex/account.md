# account

account 负责实现用户的登录和注销逻辑。

## actions.login

### 介绍

用户登录，通常情况下您需要适当修改这个方法来适配您的特殊需要。

### 参数

| 参数名 | 介绍 | 必选 | 值类型 | 可选值 | 默认值 |
| --- | --- | --- | --- | --- | --- |
| vm | vue 实例 | 必选 | Object |  |  |
| username | 账号 | 必选 | String |  |  |
| password | 密码 | 必选 | String |  |  |
| route | 重定向 | 非 | Object |  | `{ name: 'index' }` |

### 示例

``` js
this.$store.dispatch('d2admin/account/login', {
  vm: this,
  username: this.formLogin.username,
  password: this.formLogin.password
})
```

登录后重定向到指定页面：

``` js
this.$store.dispatch('d2admin/account/login', {
  vm: this,
  username: this.formLogin.username,
  password: this.formLogin.password,
  route: {
    name: 'your-page'
  }
})
```

route 字段会这样被调用：

``` js
vm.$router.replace(route)
```

route 的值可以是任何 [vue-router](https://router.vuejs.org/zh/) replace 方法的 location 参数支持的数据格式。详见 [编程式的导航](https://router.vuejs.org/zh/guide/essentials/navigation.html)

route 字段的值在下面的情况下会失效：用户在试图访问某个页面（例如：/demo/page1）时被检查到非登录状态，会被自动定向到登录页面，这时候在用户完成登录后会自动跳转到 /demo/page1 继续浏览。

## actions.logout

### 介绍

用户注销，通常情况下您需要适当修改这个方法来适配您的特殊需要。

### 参数

| 参数名 | 介绍 | 必选 | 值类型 | 可选值 | 默认值 |
| --- | --- | --- | --- | --- | --- |
| vm | vue 实例 | 必选 | Object |  |  |
| confirm | 注销确认 | 非 | Boolean |  | false |

### 示例

``` js
this.$store.dispatch('d2admin/account/logout', {
  vm: this,
  confirm: true
})
```

## mutations.load

### 介绍

用户登录后从持久化数据加载一系列的设置，例如：

* 用户名
* 主题
* 页面过渡效果设置
* 上次退出时的多页列表
* 侧边栏折叠状态

如果你扩展了系统功能并且涉及到设置项的数据持久化，不要忘了更新这里。

### 参数

无

### 示例

``` js
this.$store.commit('d2admin/account/load')
```
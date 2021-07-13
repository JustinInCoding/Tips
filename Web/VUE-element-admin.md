#### window.location.search

注意上面的search和hash的区别，如果URL中“？”之前有一个“#”比如：“\**http://localhost:63342/index.html#/version？type=35&id=5\**”那么使用window.location.search得到的就是空（“”）。因为“\**\*\*？type=35&id=5\*\**\*”串字符是属于“\**\*\*#/version？type=35&id=5\*\**\*”这个串字符的，也就是说查询字符串search只能在取到“？”后面和“#”之前的内容，如果“#”之前没有“？”search取值为空。



| Property | Value                                                 |
| -------- | ----------------------------------------------------- |
| protocol | http:                                                 |
| hostname | b.a.com                                               |
| port     | 88                                                    |
| pathname | /index.php                                            |
| search   | ?name=kang&when=2018                                  |
| hash     | #first                                                |
| host     | b.a.com:88                                            |
| Href     | http://b.a.com:88/index.php?name=kang&when=2016#first |
|          |                                                       |



#### 将get请求的参数转为Obj

```js
        GetQueryString(param) { //param为要获取的参数名 注:获取不到是为null
            var currentUrl = window.location.href; //获取当前链接
            var arr = currentUrl.split("?");//分割域名和参数界限
            if (arr.length > 1) {
                arr = arr[1].split("&");//分割参数
                for (var i = 0; i < arr.length; i++) {
                    var tem = arr[i].split("="); //分割参数名和参数内容
                    if (tem[0] == param) {
                        return tem[1];
                    }
                }
                return null;
            }
            else {
                return null;
            }
        },
```



#### Router中next的用法

```js
router.beforeEach((to, from, next) => {
  if (to.matched.some(record => record.meta.requiresAuth)) {
    // this route requires auth, check if logged in
    // if not, redirect to login page.
    if (!auth.loggedIn()) {
      next({
        path: '/login',
        query: { redirect: to.fullPath }//把要跳转的地址作为参数传到下一步
      })
    } else {
      next()
    }
  } else {
    next() // 确保一定要调用 next()
  }
})
```



#### URL 编解码

```js
encodeURIComponent
decodeURIComponent
```



#### Router 跳转

```js
this.$router.replace

// 同push用法
this.$router.push('/index')
this.$router.push({path:'/index'})
this.$router.push({path:'/index',query:{name: '123'}})
this.$router.push({name:'index',params:{name:'123'}})
```



#### npm 无效怎么办

尝试 cnpm

## 分析

PC整体布局
``` josn
html: {
    body: {
        background: #fff; font-size: 12px; line-height: 166.6%;
    }
    main: {
        header： {
            style:width: 1000px; height: 64px;
            main: {
                left：logo
                right：{
                    fun: menu
                    color: #848585
                }
            }
        }
        center：{
            style: height: 600px; background: #fff; min-width: 1000px;
            info: {
                背景：{
                    fun: 动态切换图
                }
                右：{
                    fun: 登录框功能 tabs
                    tabs: [
                        {
                            title:二维码登录
                            top: 说明文字
                            center: 图片
                            bottom: 图片 + 文字
                        }
                        {
                            title: 邮箱登录
                            top: 两个输入框有 +icon，有active,hover样式 + 左右文字
                            center: 两个按钮  有active, hover + 文字
                            bottom: 两行文字
                        }
                    ]
                }
            }
        }
        footer：{
            style: width: 1000px; margin: 0 auto; color: #848585; margin-top: 22px;
            left: logo
            center: link + icp
        }
    }
}
```

移动整体布局
``` josn
html: {
    body: {
        header: {
            top: banner
            bottom: logo
        }
        center: {
            top: 两带icon的输入框  avtive hover
            center: 文字 + 按钮hover active
            bottom: 左右文字
        }
        footer: 两行文字
    }
}
```

相对来讲PC比移动端复杂多。


### 开发
#### PC

``` bash
开发工具：VScode
开发浏览器： IE8+ Edge chrome firefox等
开发语言：html5 css3
```

定声明 html:5 回车
``` html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>邮箱</title>
</head>
<body>
    这里是内容区
</body>
</html>
```

主体布局
``` html
<div id="app">
    <!-- 头部 -->
    <header>
        <!-- logo -->
        <h1>
            <img src="#" alt="logo"/>
            <span>文字</span>
        </h1>

        <!-- 菜单 -->
        <nav>
            <a href="#">文字1</a>
            <a href="#">文字2</a>
            <a href="#">文字3</a>
        </nav>
    </header>

    <!-- 中间 -->
    <section class="main">
        <!-- 背景banner切换 -->
        <div class="banner">
            // 背景banner
        </div>
        
        <!-- login tabs切换 -->
        <div class="logo">
            // login
        </div>
    </section>

    <!-- 底部 -->
    <footer>
        <div class="logo">logo</div>
        <div class="link">link</div>
    </footer>
</div>
```

主体样式—— head 插入 
``` html
<style>
#id {}
</style>
```
# cnblogs_u
> 博客园优化
 
### 主题优化SimpleMemory
- 文档地址: https://bndong.github.io/Cnblogs-Theme-SimpleMemory/v2/#/Docs/Customization/config
- 在博客园 -> 设置 -> 博客侧边栏公告 中添加如下代码
```js
<script src="https://cdn.jsdelivr.net/gh/gityuing/cnblogs_u@main/Cnblogs-Theme-SimpleMemory/simpleMemory.js" defer></script>
<script type="text/javascript">
    window.cnblogsConfig = {
      info: {
        name: 'yuings', // 用户名
        startDate: '2021-01-01', // 入园时间，年-月-日。入园时间查看方法：鼠标停留园龄时间上，会显示入园时间
        avatar: 'https://pic.cnblogs.com/avatar/2675927/20211208200042.png', // 用户头像
      },
      banner: {
          home: {
            
          },
      },
      footer: {
        style: 1,
        text: {
          left: '星月皎洁，明河在天',
        },
      },
      articleSuffix: {
      },
    }
    document.getElementById("favicon").href="https://img.yuing.top/svg/youyu-color.svg"
</script>
```

### 添加插件,可以跟随鼠标移动的小人
- 在博客园 -> 设置 -> 博客侧边栏公告 中添加如下代码
```js

<script src="https://cdn.jsdelivr.net/gh/gityuing/cnblogs_u@main/L2Dwidget/L2Dwidget.min.js"></script>
<script>
    let display1={//大小位置什么的自己慢慢调就是了
        position: "right",//定位
        width: 130,//宽度
        height: 210,//高度
        hOffset: 10,//左右
        vOffset: 10//上下
    };
    let display2={//大小位置什么的自己慢慢调就是了
        position: "right",//定位
        width: 130,//宽度
        height: 210,//高度
        hOffset: 10,//左右
        vOffset: -40//上下
    };
    // 可选: midnight springorautumn summer winter evening 01  epsilon2_1 shizuku haru_02 z16 haru_01 hibiki tsumiki （漫画女）
    // haru_03 (可爱男)  koharu（可爱女）   izumi（女）  hijiki（黑猫）  wanko（狗子） chitose（漫画男）
    //   tororo（白猫） miku

    let pluginModelPath = 'hijiki/';
    
    L2Dwidget.init({
        pluginRootPath: "https://cdn.jsdelivr.net/gh/gityuing/cnblogs_u@main/L2Dwidget/",//资源root路径
        pluginJsPath: "js",//js相对root的路径
        pluginModelPath: 'tororo',//模型相对root的路径
        model: {
            scale: 2,
            jsonPath: "https://cdn.jsdelivr.net/gh/gityuing/cnblogs_u@main/L2Dwidget/assets/tororo/model.json"
        },
        mobile: {
            show: !1
        },
        display: display2,
        tagMode: !1,
        debug: !1,
        log: !1
    });
</script>
```

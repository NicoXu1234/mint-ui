## BUG 源码修改

***
# 1
mint-ui piker滑动穿透
node_modules/mint-ui/lib/mint-ui.common.js,
搜索picker,全匹配，匹配大小写，找到staticClass: 'picker', class: 'picker-3d'，
在第一个div下添加

```
on:{
    "touchmove":function(e){
        e.preventDefault();
        e.stopPropagation()
        }
    }
```    
    
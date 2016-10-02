# webApp必须掌握的知识点

- viewport
- 单位




## viewport

手机浏览器默认为我们做的两件事：

1.页面渲染在一个980px(ios)的viewport

2.缩放

### 设计移动web

通过meta标签：

`<meta name="viewport" content="name=value,name=value"`
```
width: 设置布局viewport的特定值（‘device-width’）
initial-scale: 设置页面的初始缩放
minimun-scale: 最少缩放
maximum-scale: 最大缩放
user-scalable: 用户能否缩放
```
```
<meta name="viewport" content="width=device-width,initial-scale=1,user-scalable=no">
```

### 使用flex布局
```
#wrap{
	display: flex;
}
.item {
	flex: 1;
}
```

```
不定宽高的水平垂直居中
1.translate
.wrap{
	position: absolute;
	top: 50%;
	left: 50%;
	z-index: 3;
	-webkit-transform: translate(-50%, -50%);
}
2.flex
.parent{
	justify-content: center;
	align-items: center;
	display: flex;
}
```

flex的兼容性
ios可以使用最新的flex布局
Android4.4以下，使用旧版本的flex
Android4.4以上的，使用最新的flex

```
新的flex布局：
display: -webkit-flex;
-webkit-flex: 1;
justify-content: center;
align-items: center;

旧的flex布局：
display: -webkit-flex-box;
-webkit-flex-box: 1;
box-pack: center;
box-align: center;
```
### 响应式设计
```
使用媒体查询
@media screen and (max-width: 920) {}

媒体类型：
screen(屏幕)
print(打印机)
handheld(手持设备)
all(通用)

常用媒体查询参数：
width、height 视口宽高
device-width  设备的宽度
device-height  设备的高度
orientation  检查设备处于横向还是竖屏
```

### 相对单位

- em
- rem 根据html的大小设置
	
	rem的基本值
	rem = screen.width/20
```
//默认320px
html{
	font-size: 32px;
}
//iphone 6
@media (min-device-width: 375px) {
	html{
		font-size: 37.5px;
	}
}
//iphone 6s
@media (min-device-width: 414px) {
	html {
		font-size: 41.4px;
	}
}
```












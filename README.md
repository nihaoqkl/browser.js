browser.js v0.6
==========

最靠谱的浏览器嗅探方式
--------------------------------------
### 浏览器内核判断
```Javescript
browser.msie			//IE下返回IE的文档模式，怪癖模式返回5
browser.rv				//IE下返回真实的IE版本号，其他浏览器返回UserAgent中rv字段的值
browser.WebKit			//Chrome或Safari等webkit内核浏览器下返回webkit版本号
browser.Opera			//Opera下 返回Opera版本号
browser.Gecko			//Firefox中返回Gecko版本号
browser.Chrome			//基于Chromium二次开发的浏览器中返回Chrome版本号
```
### 浏览器语言判断
```Javescript
browser.language		//返回浏览器语言，如“zh-CN”
```

### 浏览器外壳判断
```Javescript
browser.Edge			//微软Win10中的Edge浏览器下返回版本号(此浏览器为Chromium内核)
browser.Safari			//Safari下返回Safari版本号
browser.Chrome			//Chrome下返回Chrome版本号
browser.Maxthon			//遨游高速模式返回版本号
browser.CoolNovo		//枫树浏览器高速模式返回版本号
```

### 特性：
- 支持IE5-IE11、Webkit、Gecko、Presto内核浏览器
- 遵循define.amd\define.cmd标准，使用RequireJS或seajs时，自动注册为其匿名模块
- 没有define函数时，优先注册为$.browser或者window.browser
- 能获取版本号的浏览器或内核的版本号时，优先返回版本号，无版本号返回bool值

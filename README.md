responsiveWeb
===========================
> 响应式开发网站[CSS3, HTML5]

### 项目页面
从左到右依次为宽度1349px（大屏幕）、800px（中屏幕）、480px（小屏幕）的浏览器截图
![pageScreenShot](https://github.com/ickedesign/responsiveWeb/blob/master/pageScreenShot.jpg)

### 项目心得
1. 响应式网站断点的选择：不针对特定的设备进行选择，而是根据屏幕来划分
2. HTML5语义化标签的使用，比如标签`header`,`footer`,`nav`,`section`,`b`,`em`,`i`等
3. px、em、rem的不同。em是相对父元素的字体大小，rem的相对参照物是根元素html的字体大小。默认为16px。一般会把html元素的font-size设为62.5%，即10px。但有些浏览器的默认最小字体大小为12px，此时62.5%的字体大小为12px
4. CCS3的选择器使用，比如`::selection {}`用于设置选中文字的样式，`nth-child(n)`的使用等等
5. 对于浮动导致的高度塌陷，清除浮动的布局clearfix的书写
6. 对于设置`display: inline-block`的空白间隙的解决措施：①设置父节点的样式为`font-size: 0`，子元素重新设置字体大小，但这又重新引入了一些副作用，比如：下边距的出现；②去除`li`与`li`标签的间隙，或者删去`</li>`；③设置负边距，不过在不同浏览器下负边距的设置是不同的。所以我觉得第二种比较好
7. 使用CSS雪碧图来减少http请求数目和混乱加载
8. 一些布局上的小技巧，比如：`text-indent: -999rem`可以把文字隐藏，不换行的样式设置(`text-overflow: ellipsis;`, `overflow: hidden;`, `white-space: nowrap;`)
9. `calc`是CSS3的一个计算属性，通过动态计算获取长度值，小数越精确，算出的差异越小。比如：`width: calc(33.3333333333% - 3rem);`
10. `filter: greyscale(100%);`（需加兼容前缀）在项目中处理图片的使用
11. 媒体查询media query的使用，比如一般的写法为`@media only screen and (min-width: 481px) and (max-width: 800px) {}`
12. Chrome的布局调试工具的使用
13. media query媒体查询在html元素的级别之上，所以`font-size`是相对于浏览器的默认值换算的，即1rem = 16px。比如`@media only screen and (max-width: 50rem) {}`，这里指的是800px。由于em的兼容性比rem好，我们这里也可以把rem替换为em。当浏览器的字体发生改变时，样式也会发生改变

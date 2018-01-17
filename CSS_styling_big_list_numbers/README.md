## CSS 技巧
* 改变列表数字样式
1. 去除默认列表数字
```css
ol.country {
	margin: 0;
	padding: 0;
	list-style-type: none;
}
```
2. counter-increment 属性
```css
ol.country li {
	margin: 0;
	position: relative;
	color: #ccffff;
	padding: 25px 0 0 70px;
	counter-increment: myCounter;
}
```
3. list-style-type 属性
```css
ol.country li::before{
	content: counter(myCounter,decimal-leading-zero);
	display: inline-block;
	padding: 0;
	font-size: 5.3em;
	text-align: right;
	color: #003366;
	font-family: 'Microsoft YaHei',serif;
	position: absolute;
	top: 5px;
	left: -30px;
}
```
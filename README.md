# CodeWarsNotes
平时练习的时候总结的一些go语言的小知识点，感兴趣的可以<font color="yellow">*star*</font>支持一下<br />
> 微信公众号--go学习
***
### 基本知识点
- 不能修改原始字符串<br />
```go
var str string = "hello"
s[0] = 'w' //报错，cannot assign to s[0]
/**********************/
/*如何修改字符串呢*/
/**********************/
newStr := []byte(str) //转化为byte切片
newStr[0] = 'w'
str = string(newStr)  //再转换为string类型
```
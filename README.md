# CodeWarsNotes
平时练习的时候总结的一些go语言的小知识点，感兴趣的可以<font color="yellow">*star*</font>支持一下<br />
欢迎关注本人微信公众号 :point_right: go学习
***
### 目录 <br />
#### <a href="#fundmental">基本知识点</a> <br />
&nbsp; &nbsp; <a href="#string">字符串</a> <br />
&nbsp; &nbsp; <a href="#string">TODO</a> <br />
&nbsp; &nbsp; <a href="#string">TODO</a> <br />

### 基本知识点
#### <a name="string">【字符串】</a>
- 字符串是不可变的:x:<br />
```go
var str string = "hello"
s[0] = 'w' //报错，cannot assign to s[0]

/*如何修改字符串呢*/
newStr := []rune(str) //转化为rune切片,不转化为byte切片，从而字符可以扩大范围至unicode
newStr[0] = []rune("王")[0]
str = string(newStr)  //再转换为string类型
fmt.Println(str) // 王ello
```
>注意事项 <br />
```go
str := "王"
fmt.Println([]byte(str)) // [231 142 139]
fmt.Println([]rune(str)) // [29579]
fmt.Println(rune(str))   //!报错 cannot convert "王" (type untyped string) to type rune
```
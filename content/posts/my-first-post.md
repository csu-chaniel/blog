+++
title = '[Golang] %v、%+v 和 %#v 的区别'
date = 2024-10-20T10:48:30+08:00
draft = false
+++
在 Go 语言中，fmt 包提供了多种格式化输出方式，其中 %v、%+v 和 %#v 是用于格式化结构体的常用占位符。它们的区别如下：

1. %v
- 基本格式化。
- 对于结构体，会输出字段的值。
```go
type Person struct {
    Name string
    Age  int
}

p := Person{"Alice", 30}
fmt.Printf("%v\n", p) // 输出：{Alice 30}
```
2. %+v
- 增强格式化。
- 对于结构体，会输出字段的名称和值。
```go
fmt.Printf("%+v\n", p) // 输出：{Name:Alice Age:30}
```
3. %#v
- 完整格式化。
- 输出 Go 语言语法格式的表示，通常用于生成可以直接用作代码的输出。
```go
fmt.Printf("%#v\n", p) // 输出：main.Person{Name:"Alice", Age:30}
```
这三种格式化方式可以帮助开发者在调试和日志记录时更好地查看结构体的内容。

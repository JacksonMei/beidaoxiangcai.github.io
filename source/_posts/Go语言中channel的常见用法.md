---
title: Go语言中channel的常见用法
date: 2019-02-28 16:58:57
tags: K8S
index_img: /img/page/go.png
---

## channel基本用法



## channel骚操作

#### 校验channel是否关闭

```go
if v, ok := <- ch; ok {
    fmt.Println(v)
}
```

#### 控制函数并发度

如下函数test在多个线程中运行，但同时并发只能有5个实例，如在redis 连接池的处理

```go
ch := make(chan string, 5)

func test() {
    ch <- "test start"
    defer func() {
        <-ch
    }
    // do something
    ... 
}
```

### ！未完待续
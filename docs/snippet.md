# snippet模块用于自定义关键字

## 自定义关键字
无论是接口测试，还是UI自动化测试，我们都会遇到框架自身赋予的能力难以满足测试需求的境况。此时我们需要代码来扩展框架功能。
测试数据在整个测试过程中会在不同处理阶段进行传递，测试数据的格式已经预定义好，这样我们可以很方便的通过代码处理测试数据。
如果你需要写一个函数来处理测试数据，那么你可以向下面这样定义一个函数：
`def test(data):
    print("这是一个关键字用法示例")
    return data`
当框架执行遇到 @{test} 时会自动将当前测试数据传入test函数并执行。
使用关键字有如下限制请遵守
* 函数只有一个参数且函数声明时必须有一个参数
* 函数必须将传递的参数返回
* 函数名必须与@{}里的调用名称一致

## 调试关键字
自定义关键字时若需要调试可以构造测试输入，测试数据仅支持json格式。
测试数据和自定义关键字会同时发送给flask后端，后端接收到调试请求时会先将测试数据使用json.loads方法转换为python对象。
之后测试数据会自动传入到自定义关键字中并执行自定义关键字，若执行成功则讲执行后的测试数据再页面上替换掉请求时的数据。

## 接口测试中使用

## 自动化测试中使用
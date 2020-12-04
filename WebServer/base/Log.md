# 日志设计

## 日志作用

1. 开发
   * 调试
   * 理解程序
2. 运行
   * 诊断系统故障并处理
   * 记录运行状态

## 日志级别

* TRACE :比DEBUG更细的事件，开发过程中使用
* DEBUG
* INFO
* WARN
* ERROR
* FATAL

## Logger使用的时序图



Logger => impl => LogStream =>operator  << FixedBuffer  => g_output =>g_flush

Logger：日志类

implement：实际格式化实现

LogStream：主要用来格式化输出，重载了<<运算符，同时也有自己的缓冲区FixedBuffer。

FixedBuffer：缓冲区

g_output：标准输出的缓冲区

g_flush：清空




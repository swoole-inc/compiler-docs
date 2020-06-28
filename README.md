# Swoole Compiler

* 保护程序源码：避免 PHP 源代码泄漏，避免被编辑
* 提升性能：使用`Swoole Compiler`底层内置了多个编译优化器，可优化`opcode`，性能比源码执行有较大提高
* 授权管理：内置了授权管理功能，可限制`PHP`程序运行的机器硬件和网络环境

与`Zend Guard`等传统的`PHP`加密器不同，`Swoole Compiler`没有软件界面，它提供了API（终生版本提供的离线包），可将`Swoole Compiler`集成到您的打包发布平台中，完全是可编程的。

`Swoole Compiler`相比其他传统的`PHP`加密器，安全强度更高。`Swoole Compiler`使用了特殊定制的`ZendVM`，与普通的`PHP`程序运行模式有较大差异。

环境支持
------
* PHP版本：`5.4`（仅`Linux`）、`5.5`、`5.6`、`7.0`、`7.1`、`7.2`、`7.3`、`7.4`
* 操作系统：`Linux`、`Windows`、`MacOS`、`FreeBSD`
* 机器硬件：`Intel/AMD x86-64`、`ARM64`
* 线程安全：同时支持线程安全和非线程安全两种模式
* 使用限制：
 * 目前仅支持`64`位版本的`PHP`，不支持`32`位版本
 * `Windows`平台下只支持`PHP-5.5`或更高版本，不支持`5.4`以下版本（包括`5.4`）
 * 不支持`xdebug`或者其他`HOOK`了`opcode handler`的扩展
 * 不支持`Debug`版本的`PHP`环境
* **`Compiler`离线版加密器仅支持`Linux`平台，`Loader`加载器可支持全部平台**
* **`Compiler`离线版加密器仅授权过的机器可运行**

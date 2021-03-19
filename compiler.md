# Swoole Compiler

* 保护程序源码：避免 PHP 源代码泄漏，避免被编辑
* 提升性能：使用`Swoole Compiler`底层内置了多个编译优化器，可优化`opcode`，性能比源码执行有较大提高
* 授权管理：内置了授权管理功能，可限制`PHP`程序运行的机器硬件和网络环境

与`Zend Guard`等传统的`PHP`加密器不同，`Swoole Compiler`没有软件界面，它提供了API（终生版本提供的离线包），可将`Swoole Compiler`集成到您的打包发布平台中，完全是可编程的。

`Swoole Compiler`相比其他传统的`PHP`加密器，安全强度更高。`Swoole Compiler`使用了特殊定制的`ZendVM`，与普通的`PHP`程序运行模式有较大差异。

环境支持
------
* PHP版本：`5.4`（仅`Linux`）、`5.5`、`5.6`、`7.0`、`7.1`、`7.2`、`7.3`、`7.4`、`8.0`
* 操作系统：`Linux`、`Windows`、`MacOS`、`FreeBSD`
* 机器硬件：`Intel/AMD x86-64`、`ARM64`
* 线程安全：同时支持线程安全和非线程安全两种模式
* 使用限制：
 * 目前仅支持`64`位版本的`PHP`，不支持`32`位版本
 * `Windows`平台下只支持`PHP-5.5`或更高版本，不支持`5.4`以下版本（包括`5.4`）；Windows下推荐使用wsl环境，不支持cygwin环境。
 * 不支持`xdebug`或者其他`HOOK`了`opcode handler`的扩展
 * 不支持`Debug`版本的`PHP`环境
* **`Compiler`离线版加密器仅支持`Linux`平台，`Loader`加载器可支持全部平台**
* **`Compiler`离线版加密器仅授权过的机器可运行**

>[danger] 推荐使用`PHP7`版本，安全性较高

线程安全
----
如果使用的`PHP`为线程安全版本，请下载线程安全版本的`Loader`。可以通过`php -i |grep Thread`或`phpinfo()`查看当前`PHP`是否为线程安全版本。

调试版本
----
请勿使用`Debug`版本的`PHP`，使用 `php -i | grep -i debug`查看是否有`Debug Build => yes`

另外，可修改`php.ini`将`display_startup_errors = on`开启扩展加载错误日志。

使用须知
----
* 编译和运行环境所使用的`Swoole Compiler`必须一致，如运行环境是`5.6`，那么必须使用`5.6`版本的`Swoole Compiler`来进行编译，否则无法运行

产品价格
----
|  有效期 | 价格  |
| ------------ | ------------ |
| 1年  | [3000](https://business.swoole.com/order/index/?pay_type=pay_by_year)  |
|  终生 |  [10000](https://business.swoole.com/order/index/?pay_type=pay_by_all) |
|  定制 |  [50000](https://business.swoole.com/order/index/?pay_type=pay_by_made) |

> 价格含税，可开具增值税普通发票、增值税专用发票

有效期仅限制编译端，客户端不受有效期影响。如您购买了1年授权，那仅在授权有效期内可以对PHP程序进行编译。超过有效期后，不能再对新的程序进行编译，但是已编译好的程序，不受影响，仍然可以使用。

目前`Swoole Compiler`会限制运行编译器程序的`Mac`地址。

付款方式
----

* [微信支付](https://business.swoole.com/order/index/)
* [支付宝](https://business.swoole.com/order/index/)
* [对公账户转账](https://business.swoole.com/payinfo.html)

商业支持
----
<img src="https://www.swoole.com/static/uploads/wiki/201901/26/723430445099.png" width = "300" height = "300" alt="微信" />

* 付款完成后，添加微信，提供技术支持服务
* 我们会向您以邮件方式发送`Swoole Compiler`的二进制软件，并提供一对一的工程师技术支持
* 在技术支持服务期内我们会提供`7天 x 8小时` 商业支持，为您解决问题
* 在授权有效期内可免费升级版本，或更换授权机器
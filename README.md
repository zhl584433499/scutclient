scutclient
=================

# 特性

* 可选[luci](https://github.com/scutclient/luci-app-scutclient)界面
* 采用socket raw，减少libpcap等等的第三方库的依赖
* 单线程

# OpenWrt编译方法

* openwrt目录重命名scutclient为放在Openwrt Buildroot的package文件夹中
* 运行
```bash
make menuconfig
```
在Network中可以找到scutclient，选择*/M编译，然后保存退出
* 确保执行make后没有报错，能正常编译固件后，执行
```bash
make package/scutclient/compile V=s
```
编译程序包

# 直接编译

```bash
autoreconf -fi
./configure
make
make install
```
configure添加 `--prefix="/path/to/bin"` 可指定安装目录

运行需要root权限

# 许可证

[AGPLv3](https://www.gnu.org/licenses/agpl-3.0.html)

特别指出禁止任何个人或组织将 [scutclient](http://github.com/scutclient/) 的代码投入商业使用，由此造成的后果和法律责任均与本项目无关。 

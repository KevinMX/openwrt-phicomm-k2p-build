# openwrt-phicomm-k2p-build-config
OpenWrt/LEDE build config for Phicomm K2P Wireless router. (For my personal use&backup)

If you want to use this config file to compile your firmware, go to here first to get the source code repository and more config info:

https://github.com/coolsnowwolf/lede/

Then put the .config file under the code directory and run `make -jX V=s`, X as your CPU core number.

If I keep this file up to date, you should be able to compile your own firmware.

Use it as your own risk.


斐讯K2P的OpenWrt/LEDE编译配置文件

如果你要用本仓库的配置文件编译，建议先去lean的仓库看一下相关说明，本配置文件为lean的OpenWrt源码生成，本意是个人使用以及备份。

将.config文件放置在源代码根目录下运行`make -jX V=s`即可编译，其中X为CPU线程数。

如果本文件及时更新，应该是能正常编译固件的（指openwrt代码仓库没有问题的情况下）

请自行斟酌使用，如出现任何问题后果自负。

# openwrt-phicomm-k2p-build
## 斐讯K2P的OpenWrt/LEDE编译配置文件及预编译固件（自用&备份用）

如果你要用本仓库的配置文件编译，建议先去[lean的仓库](https://github.com/coolsnowwolf/lede/)看一下相关说明，本配置文件为lean的OpenWrt源码生成，本意是个人使用以及备份。

出于稳定性考虑暂时不使用mt76开源驱动，请使用此处的[闭源驱动](https://github.com/MeIsReallyBa/k2p-openwrt-mt7615_5.0.2.0)。

将.config文件放置在源代码根目录下运行`make -jX V=s`即可编译，如提示out of sync请重新运行`make menuconfig`然后保存再进行编译。其中X为CPU线程数。

编译教程参考：[OpenWrt/LEDE编译小记（斐讯K2P）](https://www.jianshu.com/p/eed71e8a22cc)

如果本文件及时更新，应该是能正常编译固件的（指openwrt代码仓库没有问题的情况下）

请自行斟酌使用，如出现任何问题后果自负。

自用插件列表：

```luci-app-accesscontrol
luci-app-arpbind
luci-app-autoreboot
luci-app-ddns (已包含阿里云/cloudflare等ddns脚本)
luci-app-familycloud (电信家庭云提速)
luci-app-filetransfer
luci-app-firewall
luci-app-flowoffload
luci-app-nlbwmon (带宽监控)
luci-app-ramfree
luci-app-sqm (已包含额外的SQM脚本)
luci-app-ssr-plus (v2ray+Kcptun+ShadowsocksR&服务端)
luci-app-statistics
luci-app-upnp
luci-app-vlmcsd (KMS服务器)
luci-app-wifischedule
luci-app-wol (网络唤醒)
luci-theme-argon
ipv6helper
mtk 5.0.2.0闭源驱动
```
TODO: 内存/闪存 自适应，参考：https://github.com/coolsnowwolf/lede/issues/1507
咱的k2p没有硬改，用不到这个功能，所以有可能永远也不会加进去（逃

***

## OpenWrt/LEDE build config and prebuilt firmware images for Phicomm K2P Wireless router. (For my personal use&backup)

If you want to use this config file to compile your firmware, go to [here](https://github.com/coolsnowwolf/lede/) first to get the source code repository and more config info:

Due to stability reasons, not using mt76 open source driver for now. Please check [here](https://github.com/MeIsReallyBa/k2p-openwrt-mt7615_5.0.2.0) for closed source driver.
Then put the .config file under the code directory and run `make -jX V=s`, X as your CPU core number. If prompt "out of sync" simply run `make menuconfig` again then compile.

If I keep this file up to date, you should be able to compile your own firmware.

Use it as your own risk.

A brief list for the stuff that I use:

```luci-app-accesscontrol
luci-app-arpbind
luci-app-autoreboot
luci-app-ddns (including extra scripts for aliyun, cloudflare, etc)
luci-app-familycloud (China Telecom Network boost tool/FamilyCloudSpeeder)
luci-app-filetransfer
luci-app-firewall
luci-app-flowoffload
luci-app-nlbwmon (Netlink based bandwidth accounting)
luci-app-ramfree
luci-app-sqm (including extra scripts)
luci-app-ssr-plus (v2ray+Kcptun+ShadowsocksR&server)
luci-app-statistics
luci-app-upnp
luci-app-vlmcsd (KMS Server)
luci-app-wifischedule
luci-app-wol (Wake on Lan)
luci-theme-argon
ipv6helper
mtk 5.0.2.0 closed source driver
```
TODO: RAM/flash size auto detect, since I did not hard-modded my k2p, so maybe it will never be implemented ;) Here's an example of how to do this: https://github.com/coolsnowwolf/lede/issues/1507
# openwrt-phicomm-k2p-build
## 斐讯K2P的OpenWrt/LEDE编译配置文件及预编译固件（自用&备份用）

如果你要用本仓库的配置文件编译，建议先去[lean的仓库](https://github.com/coolsnowwolf/lede/)看一下相关说明，本配置文件为lean的OpenWrt源码生成，本意是个人使用以及备份。

~~出于稳定性考虑暂时不使用mt76开源驱动，请使用此处的[闭源驱动](https://github.com/MeIsReallyBa/k2p-openwrt-mt7615_5.0.2.0)。~~
目前使用Lean已在源码中集成的驱动(package/lean/mt)，如出现问题请及时向上游反馈。

将.config文件放置在源代码根目录下运行`make -jX V=s`即可编译，如提示out of sync请重新运行`make menuconfig`然后保存再进行编译。其中X为CPU线程数。如需已编译好的固件请在[releases](https://github.com/KevinMX/openwrt-phicomm-k2p-build/releases/)中自取。

编译教程参考：[OpenWrt/LEDE编译小记（斐讯K2P）](https://mary.kevinmx.tk/index.php/archives/4/)

如果本文件及时更新，应该是能正常编译固件的（指openwrt代码仓库没有问题的情况下）

请自行斟酌使用，如出现任何问题后果自负。

自用插件列表：

```luci-app-accesscontrol
luci-app-arpbind
luci-app-autoreboot
luci-app-ddns (包含额外的ddns脚本)
luci-app-firewall
luci-app-flowoffload
luci-app-ramfree
luci-app-sqm
luci-app-ssr-plus (v2ray+trojan+ShadowsocksR&服务端)
luci-app-v2ray-server
luci-app-upnp
luci-app-vlmcsd (KMS服务器)
luci-app-wifischedule
luci-app-wol (网络唤醒)
luci-theme-argon
ipv6helper
集成无线驱动
```

***

## OpenWrt/LEDE build config and prebuilt firmware images for Phicomm K2P Wireless router. (For my personal use&backup)

If you want to use this config file to compile your firmware, go to [here](https://github.com/coolsnowwolf/lede/) first to get the source code repository and more config info:

~~Due to stability reasons, not using mt76 open source driver for now. Please check [here](https://github.com/MeIsReallyBa/k2p-openwrt-mt7615_5.0.2.0) for closed source driver.~~
Using Lean's built-in wireless driver(/package/lean/mt).

Then put the .config file under the code directory and run `make -jX V=s`, X as your CPU core number. If prompt "out of sync" simply run `make menuconfig` again then compile. Go to [releases](https://github.com/KevinMX/openwrt-phicomm-k2p-build/releases/) for prebuilt images if you prefer.

If I keep this file up to date, you should be able to compile your own firmware.

Use it as your own risk.

A brief list for the stuff that I use:

```luci-app-accesscontrol
luci-app-arpbind
luci-app-autoreboot
luci-app-ddns (including extra scripts)
luci-app-firewall
luci-app-flowoffload
luci-app-ramfree
luci-app-sqm
luci-app-ssr-plus (v2ray+trojan+ShadowsocksR&server)
luci-app-v2ray-server
luci-app-upnp
luci-app-vlmcsd (KMS Server)
luci-app-wifischedule
luci-app-wol (Wake on Lan)
luci-theme-argon
ipv6helper
wireless driver built-in
```

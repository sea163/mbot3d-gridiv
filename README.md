# mbot3d-gridiv
关于 mbot3d gridiv 3d 打印机的一些资料

# 控制板
* 主板: MekerBase MKS Gen LV1.0
* 屏幕: MekerBase MKS TFT35 V1.0 (无WIFI模块)
* 驱动模块: MKS 8825 V1.2
* 断料检测连载在屏幕控制板 XS12-PB1
* 原始屏幕中固件信息 Type:MBot Grid 4 Firmware: 1.0.1 Magicfirm

# 驱动参考电压
* X: 0.404V 对应 0.808A
* Y: 0.403V 对应 0.808A
* Z: 0.341V 对应 0.682A
* E1: 0.352V 对应 0.704A

# firmware Marlin-2.1.3-b2_MKS Gen LV1.0.hex
* 刷机COM1改为自己主板的串口号
* ```avrdude "-Cavrdude.conf" -v -V -patmega2560 -cwiring "-PCOM1" -b115200 -D "-Uflash:w:Marlin-2.1.3-b2_MKS Gen LV1.0.hex:i"```
* 启用线性提前功能
* 三点调平坐标 X239 Y219,X65 Y219,X239 Y2
* TFT35 固件为MKS官网最新 V1.0.8
* 注:由于我的原始固件丢失,打印板3颗磁铁也都掉了三点调平的坐标点可能与原厂固件有差异

# asrock-B460M-ITX-ac
华擎b460m-ixt/ac 10400

### 记录待明确项目
* booter -> Quirks -> resizeAppleBars 
If your firmware supports increasing GPU Bar sizes (ie Resizable BAR Support), set this to 0
看bios能不能开
* kernel -> Quirks -> disableIOmapper 
Not needed if VT-D is disabled in the BIOS ,准备在bios里打开vd-t


## 硬件信息
| 类型 | 名称 | 说明 |
| :--- | :---| :--- |
| cpu | i5 10500 es QSRK | 全核心3.7GHZ |
| 主板 |  asrock-B460M-ITX-ac | 自带wifi，更换了BCM94352z, 联想的拆机，驱动不成功，放弃了 |
| 内存 | 酷兽 16G 2666 | |
| 独显 | rx460 4G | 后来加的，一开始用的核显卡， 接双屏幕加了独显， 讯景的， 要刷华硕的bios，否则驱动不了 |
| 硬盘 | 致态pc005 512G | m.2 接口 |

## 注意事项
* 显卡要注意品牌， 最好还是华硕或者蓝宝石的， 看网上都说讯景驱动不了， 试了一下确实不能驱动
* 工具包里有刷显卡bios工具， 这里不是教刷显卡的教程， 刷机有风险，一开始我刷了蓝宝石的vbios，导致显卡变砖，好在有核显又救回来了， 最后刷上华硕的bios，免驱成功

* 三码已删

* DeviceProperties -> Add -> PciRoot(0x0)/Pci(0x2,0x0)-> AAPL,ig-platform-id
```
无独显时配置成 07009B3E
有独显时，配置成 0300C89B
请自行修改
```

* NVRAM -> Add -> 7C436110-AB2A-4BBB-A880-FE41995C9F82
```
如果独立显卡是rx5000 | rx6000系列， 启动参数要加上 agdpmod=pikera
```

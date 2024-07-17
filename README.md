## 解密复制门禁卡与导入小米钱包

### 教程

解密dump：
https://blog.csdn.net/huliNo1/article/details/136156692

手机模拟门禁卡教程：
https://nfctool.cn/nfcphone_phone

### 密钥

`nf`中是已经分割好的keys，来自

https://github.com/hugh999999/nfc_tool_share_key

### 软件下载

#### NFC Tool

https://nfctool.cn/download

在MIUI14系统下，key和dump文件的存放路径分别为

- /storage/emulated/0/NfcTools/keyFile

- /storage/emulated/0/NfcTools/dumpFile

#### Mifare Classic Tool

*可选*

https://github.com/ikarus23/MifareClassicTool/releases/tag/v4.2.2

在MIUI14系统下，key和dump文件的存放路径分别为

- /data/user/0/de.syss.MifareClassicTool/files/MifareClassicTool/key-files

- /data/user/0/de.syss.MifareClassicTool/files/MifareClassicTool/dump-files

### 准备

- NFC手机一台
- CUID白卡两张
  https://tb.alicdn.com/
- 读卡器/另一台NFC手机(用于写入小米钱包)

### 实测结果

*仅供参考*

- 仅模拟卡ID，导入小米钱包，可以解锁小区门，无法用于楼栋门/电梯
- 写入解密dump的新卡(与原卡所有扇区每位完全一致)可以解锁小区门/楼栋门/电梯
- 导入小米钱包的卡(与原卡差别仅有扇区0第一行后半部分不一致，其余扇区完全一致)，可以解锁小区门/楼栋门，无法用于电梯

# SCUMakerLocker
SCUMakerLocker 用于SCUMaker门锁的开发与维护

## 设计规划
1. 分体设计，设计一个核心主控版，用于连接主要外设，支持联网/离线方式开门
2. 核心板功能明确，就是无线接入和控制电磁锁
3. 小板进行功能拓展，例如不同的开门方式，例如NFC、密码、指纹、人脸等

### 设计注意事项
1. 优先完成核心板设计，确定其设计方案后，验证固化，避免重复修改
2。功能模块尽量在小板上实现，考虑断网等情况。

### 核心板思路
1. 输入电压12V 为门锁供电 
2. DCDC降压 经过一路LDO为主控供电
3. 继电器两个，用于控制两个门锁
4. 考虑外挂一个8266实现ESPNOW协议链接，方便本地无网络极限条件下使用


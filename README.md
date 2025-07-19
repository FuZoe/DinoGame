# 基于stm32的谷歌小恐龙游戏（Google Chrome's Dino Game on STM32）

演示视频：https://www.bilibili.com/video/BV1MAuXzeEiJ/

## 元件清单 (components list)
- stm32f103c8t6
- OLED ssd1306 (128*64)
- 2个按键(2 button)

## 使用说明 (usage)

- 使用keil5导入工程 
- IO连接关系
  - PB3 --- OLED SCK
  - PB4 --- OLED SDA
  - PB0 --- 开始/重新开始按键 (start/restart button)
  - PB1 --- 跳跃按键 (jump button)

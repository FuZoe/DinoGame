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

## Note：
模块：分为输入处理模块、游戏逻辑模块、显示驱动模块。
原理解释：
游戏需要实时响应按键输入和画面刷新。使用了硬件定时器来控制游戏主循环的刷新频率，并通过中断立即响应用户操作，保证游戏体验流畅。以按键中断为例：当用户按下跳跃键时，GPIO 引脚触发中断，进入中断服务函数，将恐龙角色状态设置为“跳跃”，然后迅速返回主循环，由主循环完成跳跃动画和位置更新。

# 1.STM32CubeMX配置

STM32F103C8T6开发板板载LED：PC13，低电平点亮

**所有外设均使用LL库进行开发**

# 2.业务代码

GPIO输出高低电平：

```c
  LL_GPIO_SetOutputPin(LED_user_GPIO_Port, LED_user_Pin);   // 控制GPIO输出高电平
  LL_GPIO_ResetOutputPin(LED_user_GPIO_Port, LED_user_Pin); // 控制GPIO输出低电平
```

翻转GPIO电平：

```c
    LL_GPIO_TogglePin(LED_user_GPIO_Port, LED_user_Pin); // 翻转GPIO的高低电平
```

延时函数：

```c
 LL_mDelay(100); // ms延时
```


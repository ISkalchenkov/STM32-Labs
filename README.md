**Проекты Keil uVision 5**

**МК: STM32F107VC (отладочная плата STM3210C-EVAL)**

# Лабораторная работа №1 (Lab 1 - Hello World)
## Hello World!

Проект "Hello World!", реализует миганием светодиодами на отладочной плате.

В папке `StdPeriphLib Version` находится версия исходников с использованием библиотеки StdPeriphLib.

# Лабораторная работа №2 (Lab 2 - Interrupts)
## Введение в прерывания

Реализовано два обработчика прерываний:
- по переполненю таймера TIM6 (раз в секунду меняется состояние светодиода)
- по внешнему импульсу на линии EXTI9 (к PB9 подключена кнопка, по нажатию меняется состояние светодиода)

# Лабораторная работа №3 (Lab 3 - UART+DMA)
## Модуль USART, DMA

Демонстрирует работу с модулем USART и два подхода к передаче данных:
- через процессор (`#define USE_DMA` должен быть закомментирован)
- через модуль DMA (`#define USE_DMA` должен быть раскомментирован)

В папке `Waveforms` лежат осциллограммы для двух варинтов передачи данных.
- [USART without DMA.png](https://github.com/Leonidov/STM32-Labs/blob/master/Lab%203%20-%20UART+DMA/Waveforms/USART%20without%20DMA.png?raw=true) - передача по USART осуществляется через процессор.
- [USART with DMA.png](https://github.com/Leonidov/STM32-Labs/blob/master/Lab%203%20-%20UART+DMA/Waveforms/USART%20with%20DMA.png?raw=true) - передача по USART осуществляется через модуль DMA.

На двух картинках:
- **Канал А (синий)** - сигнал на выводе PD7 (светодиод LED1)
- **Канал B (красный)** - сигнал на выводе PD5 (USART2 TX Remapped)

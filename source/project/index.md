---
title: 项目经历
date: 2023-08-18 13:53:08
---

# 竞赛类

## 全国大学生电子设计竞赛

本系统是一个无电动小车动态无线充电系统，采用Ti MSP430F5529 MCU控制。无线充电发射电路和发射线圈固定在小车运行线路上。无线发射包括升压电路、ACS712检流电路、半桥驱动电路，串联谐振电路。发射电路用SG3525芯片输出频率可调的PWM波配合检流电路实现电流PI闭环控制。接收电路包括并联谐振电路、整流滤波电路、超级电容储能器件。该系统在1分钟内，可使3.33F超级电容储存7V左右的电压，驱动小车沿直径为70cm的圆行驶10圈以上。

## 全国大学生智能汽车竞赛

本次竞赛直立节能组要求车模运行的能源来自于无线接收线圈感应电流提供的电能，同时要求自制无线接收系统。我们选择的是自制车模，无线充电系统采用恒功率控制方案，应用同步整流技术，Buck同步整流降压技术，理想二极管技术，最终实现了恒功率控制无线接收系统，实验过程中，峰值效率达到了73.6%。车模主控部分，我们采用了STC8A8K和STC8G2K两种控制芯片。角度闭环和速度闭环实现了智能小车的直立运行。速度的闭环输出直接叠加在小车零点角度，通过角度环目标角度的改变实现速度控制。TPS61088和TPS63070稳压电源芯片完成车模的电源管理部分。采用集成的电机驱动芯片，提高了能量密度，降低了PCB面积。

# 电路与系统类

## 基于XXX材料的兼容XXX（国家重点研发计划课题）

本人主要负责驱动电路部分。采用Xilinx Spartan 6系列FPGA系统。驱动电路采用通用 Type-C 接口 5V 单电源供电。通过 LM27761 电荷泵芯片产生负电压。数模转换器（DAC）能将FPGA系统输出的数字量转换成模拟量，此驱动电路使用三角波作为驱动波形。减法器能将 DAC 输入的波形与额外引入的参考电压 VRef 进行比较并运算，产生正负范围可变的三角波。运算后的波形驱动能力较弱，后级电路加入了一个缓冲驱动器 OPA2677。

## XXX自适应智能调控系统设计（国家科技部XXX课题）

本人主要负责驱动电路部分。FPGA为此电路的主控，其可通过温度传感器，实时地采集环境中的温度。FPGA可产生两路控制信号，经过隔离缓冲器，控制开关的开启与关断，进而控制加热片与制冷片工作，使得器件自身温度变化到所需要的值或保持器件自身温度在一定的温度范围。

## 新型自适应XXX复合结构设计

本人主要负责驱动电路部分。设计了一套90路驱动电路，使用高度集成的 DrMOS 芯片构建紧凑的 DC-DC 电路，每路最大输出电流 3A，面积小，紧凑布局，主驱动板长仅 5cm，数控驱动板长仅 4cm，模块化，可插拔设计，可放置FPGA核心板和加载 XXX 算法。

# 射频电路类

## 雷达信号测频电路

覆盖 2-4GHz 雷达波段，输入端为两级放大器，一级为 LNA，一级为 PA，保证电路能在很高的灵敏度范围内检测信号。两级射频信号限幅器，防止输入信号过大损坏后级电路。后级为XXX和XXX，检测信号后转换为数字量，由 FPGA 读出。
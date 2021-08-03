# bandeja-platform
![alt text](https://github.com/MobileRoboticsSkoltech/bandeja-platform/blob/main/Images/bandeja-logo.png)
![Assembly](https://github.com/MobileRoboticsSkoltech/bandeja-platform/blob/main/Images/Assembly.gif)
![](./Images/data_flow.png)
![alt text](https://github.com/MobileRoboticsSkoltech/bandeja-platform/blob/main/Images/stm32_connections.png)
STM32F407 MCU board is used for controlling IMU module MPU-9150, obtaining accelerometer and gyroscope values, synchronizing Azure Kit with the rest of the peripherals and passing data to NUC. Communication between MCU and IMU, powered by 3.3V, is made via I2C protocol. For that purpose pins **PB6** and **PB7** are used apart from **PA6** pin as an external clock source and **PC9** one as an interrupt input. Azure is connected with mono-channel 3.5mm Jack plug wired to the **PA5** timer pin. Data passing to NUC is made via UART protocol using **PC10** and **PC11** connected to the corresponding pins on FT232 circuit as **TX (stm32) -> RX (FT232)** and **RX (stm32) <- TX (FT232)**.
![alt text](https://github.com/MobileRoboticsSkoltech/bandeja-platform/blob/main/Images/stm32_pins.png)

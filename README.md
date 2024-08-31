## STM32 Project - SPI Communication between 2 STM32 boards

The SPI Communication Service enables the transfer of ADC conversion results between two STM32 microcontrollers using the SPI protocol. This service allows the master STM32 to send ADC data, which is acquired in DMA mode, to the slave STM32.

### Key Features

- **SPI Configuration**: Set up the SPI protocol on both STM32 boards, including defining master/slave roles, clock polarity and phase, data size, and baud rate for efficient communication.

- **DMA-Enabled ADC**: Configure the ADC on the master STM32 in Direct Memory Access (DMA) mode for continuous and efficient conversion of analog signals. The results are transferred directly to a memory buffer for SPI transmission.

- **Transmit ADC Data**: Use SPI to send ADC conversion results from the master STM32 to the slave STM32. The data is sent as SPI frames, facilitating real-time data exchange.

- **Receive ADC Data**: On the slave STM32, receive and process the ADC results transmitted by the master. Implement data handling and parsing to correctly interpret incoming data.


### Usage
To use the SPI Communication Service for ADC data:
1. **Configure SPI**: Set up the SPI protocol on both STM32 boards, including defining the master and slave settings.
2. **Set Up DMA-Enabled ADC**: Configure the ADC on the master STM32 for DMA mode to ensure efficient data acquisition.
3. **Transmit Data**: Use the `SPI_TransmitADCData()` API to send ADC results from the master to the slave.
4. **Receive Data**: Use the `SPI_ReceiveADCData()` API on the slave STM32 to process the received ADC data.

This SPI Communication Service provides an efficient solution for transmitting ADC conversion results between STM32 microcontrollers, leveraging DMA mode for fast and continuous data handling.

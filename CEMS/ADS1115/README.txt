# ADS1115 Overview  

Welcome to the **ADS1115 ADC Documentation**. This repository provides a detailed overview of the ADS1115 16-bit Analog-to-Digital Converter (ADC), including its features, internal architecture, and application examples.  

---

## Features  

The ADS1115 is a high-precision, low-power ADC with an I2C interface, designed for flexible and reliable measurements. Key features include:  
- **Four Single-Ended Inputs** or **Two Differential Inputs**.  
- Sampling rates of up to **860 Samples per Second (SPS)**.  
- **Programmable Gain Amplifier (PGA)** for input ranges between ±256 mV to ±6.144 V.  
- A robust **16-bit Delta-Sigma ADC Core** for precise digital output.  
- **Digital Comparator** for monitoring thresholds.  
- Compact design with ultra-low power consumption.  

---

## Internal Block Diagram  

### 1. **Input Multiplexer (MUX)**  
- Select among **4 single-ended** or **2 differential inputs**.  
- Configured via software using the I2C interface.  

### 2. **Programmable Gain Amplifier (PGA)**  
- Adjusts input gain to maximize resolution.  
- Input ranges from **±6.144 V** (Gain = 2/3) to **±0.256 V** (Gain = 16).  

### 3. **16-Bit Delta-Sigma ADC Core**  
- Converts analog signals into high-resolution 16-bit digital data.  
- Utilizes oversampling for enhanced noise reduction.  

### 4. **Voltage Reference**  
- Built-in low-drift reference ensures consistent and accurate measurements.  

### 5. **Digital Comparator**  
- Monitors input against thresholds and triggers alerts.  

### 6. **Oscillator**  
- Provides an internal clock for ADC operations.  

### 7. **I2C Interface**  
- Facilitates easy communication with microcontrollers via two pins: **SCL** (Clock) and **SDA** (Data).  

---

## Functional Details  

### **Input Multiplexer (MUX)**  
- Supports multiple configurations:  
  - **Single-Ended Inputs**: Measure against ground.  
  - **Differential Inputs**: Measure the difference between two signals.  

### **Gain Configuration**  
- Programmable gain settings enhance resolution for different input ranges.  
- Example:  
  - Gain = 1: Input range ±4.096 V.  
  - Gain = 16: Input range ±0.256 V.  

### **Modes of Operation**  
- **Continuous Mode**: Continuous conversions for real-time data.  
- **Single-Shot Mode**: One-time conversion for energy efficiency.  

### **Data Rate Configuration**  
- Programmable from **8 SPS to 860 SPS**, balancing noise performance and speed.  

### **Comparator Functionality**  
- Acts as a monitoring tool for thresholds:  
  - **Traditional Mode**: Alert on threshold exceedance.  
  - **Window Mode**: Alert when input falls outside a range.  

---

## Applications  

- **Interfacing Sensors**: Analog-to-digital conversion for temperature, pressure, and accelerometer sensors.  
- **Battery Monitoring**: Real-time voltage monitoring for portable devices.  
- **Industrial Automation**: Measurement of control variables.  
- **Consumer Electronics**: High-precision sensor integration in smart devices.  

---

## Using ADS1115 with Arduino and Accelerometer  

### **Setup Steps**:  
1. Connect the accelerometer to the **ADS1115 analog inputs**.  
2. Use **I2C pins (SCL and SDA)** to connect the ADS1115 to Arduino.  
3. Configure the ADS1115 via I2C commands for single-ended or differential mode.  
4. Read and process the digital output on the Arduino.  

---

## Repository Contents  

- **`docs/`**: Contains detailed technical documentation and reference materials.  
- **`examples/`**: Sample Arduino sketches for interfacing with ADS1115.  
- **`images/`**: Block diagrams and pin configuration visuals.  

---

## Contribution  

Contributions are welcome! Feel free to open issues or submit pull requests for improvements.  

---

## License  

This repository is licensed under the **MIT License**.  

---  

For more information, visit the [ADS1115 Datasheet](https://www.ti.com/lit/ds/symlink/ads1115.pdf).  


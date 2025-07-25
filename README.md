# Fire Alarm & Relay Control System (IoT)

A real-time IoT system developed for remote fire alarm control, relay operation, and sensor monitoring in commercial buildings.

## Tech Stack
- STM32 (C++)
- Golang (Gin, MQTT, Concurrency, Redis)
- MariaDB, UART, GPIO, AWS EC2
- Firebase Cloud Messaging

## Highlights

### MQTT Broker in Go
- Built a concurrent MQTT service in Golang using goroutines and channels.
- Handled high-throughput message processing: analyzed incoming messages, checked analog sensor values and port states, and stored logs in MariaDB.
- Used Redis to temporarily store device data and cached state.
- Integrated Firebase Cloud Messaging to send real-time notifications based on sensor triggers.

### REST API with Gin
- Developed RESTful APIs using Gin for managing users, buildings, and device configurations.
- Implemented permission-based access control.
- Used `go test` to write unit tests and ensure API stability.

### Embedded STM32 Firmware
- Implemented MQTT-based communication for real-time status exchange of sensors and relays.
- Supported configuration of device settings like ports, threshold values, and operational parameters.
- Used USART (Serial) for static network configuration when needed.
- Leveraged EEPROM for storing configuration data in non-volatile memory to retain settings after power cycles.

> 🚫 **Code not public due to company policy. This repository serves as a project overview only.**

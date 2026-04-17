#ble #bluetooth
# Introduction
- a wireless communication protocol for **short-range**, **low-power** data exchange
- Part of larger [[Bluetooth]] specification but is optimized for devices that need to run for long periods on small batteries
- Regular Bluetooth continuously streams data (ie: audio) and its power usage is very high
- Tradeoff: very little power -> send small amounts of data periodically
- BLE is designed for:
	- Sensors
	- IoT
	- Wearables
	- Control Systems
# Architecture
- client-server model
	- **Peripheral** (Server) - IoT device
	- **Central** (Client) - Mobile Application
- Roles
	- Peripheral - [[Advertising packets|advertises]] itself, holds data/services, and waits for connection
	- Central - scans for devices, connects, reads/writes data
# Services and Characteristics
- Device -> Contains **Services** -> contains **Characteristics**
- Characteristics
	- Support:
		- Read (get value)
		- Write (send command)
		- Notify (device pushes updates)
# Communication Flow
1. Peripheral starts advertising
2. Central scans and finds device
3. Central connects
4. Central discovers services
5. Central reads/writes characteristics
# Important Concepts
- [[Generic Attribute Profile (GATT)]] - how services/characteristics are structured
- [[UUIDs]] - Unique identifiers for services and characteristics
- [[Advertising packets]] - how peripheral announces itself
- [[Connection Interval]] - tradeoff between speed and power usage



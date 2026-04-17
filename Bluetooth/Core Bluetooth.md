#bluetooth #ble 
Reference: 
- [Core Bluetooth Archived Docs]([https://developer.apple.com/library/archive/documentation/NetworkingInternetWeb/Conceptual/CoreBluetooth_concepts/CoreBluetoothOverview/CoreBluetoothOverview.html](https://developer.apple.com/library/archive/documentation/NetworkingInternetWeb/Conceptual/CoreBluetooth_concepts/CoreBluetoothOverview/CoreBluetoothOverview.html "https://developer.apple.com/library/archive/documentation/NetworkingInternetWeb/Conceptual/CoreBluetooth_concepts/CoreBluetoothOverview/CoreBluetoothOverview.html"))
- [Core Bluetooth API Ref]([https://developer.apple.com/documentation/corebluetooth/](https://developer.apple.com/documentation/corebluetooth/ "https://developer.apple.com/documentation/corebluetooth/"))

- Apple's Core Bluetooth framework lets iOS apps communicate with [[Bluetooth Low Energy (BLE)|BLE]] devices 
# Representing Centrals, Peripherals, and [[Peripheral Data Structure|Peripheral Data]]
## Central Side
- Most bluetooth transactions will be on the central side
- A local central device is represented by a `CBCentralManager` object
	- Used to manage discovered or connected remote peripheral devices which are represented by `CBPeripheral` objects
- Services of remote peripheral are represented by `CBService` objects
- Characteristics are represented by `CBCharacteristic objects`
## Peripheral Side
- Local peripheral is represented by `CBPeripheralManager`
- Remote central devices is represented by `CBCentral` object
- Services are represented by `CBMutableService` object
- Characteristics are represented by `CBMutableCharacteristic` object

#ble #bluetooth
# Services & Characteristics
- Peripherals can contain one or more services
- A service is a collection of data and behavior for accomplishing a function or feature of a device
- Services are made up of characteristics or included services (references to other services)
- A characteristic contains further details about peripheral's service
# How Centrals Interact
- After a central has connected to peripheral, it can discover the full range of services and characteristics offered
- A central can interact with a service by reading or writing values to a characteristic
- ie: app may request current room temp from digital thermostat, or can provide thermostat with value to set room temp
#ble #bluetooth 
- React Native wrapper around [[Core Bluetooth]] and [[Bluetooth Low Energy (BLE)]]
- Code snippets in this file
# Scan And Connect (Central)
```tsx
export async function scanAndConnect(): Promise<Device> {
    const manager = getManager();
    return new Promise<Device>((resolve, reject) => {
        let settled = false
        const timeoutId = setTimeout(() => {
            if (settled) return;
            settled = true;
            manager.stopDeviceScan();
            reject(new Error('Could not find relay device'))
        }, 10000)
        manager.startDeviceScan(null, null, async (error, device) => {
            if (error) {
                if (settled) return;
                settled = true;
                clearTimeout(timeoutId);
                manager.stopDeviceScan();
                reject(error);
                return
            }
            if (!device) return;

            const deviceName = device.name ?? device.localName ?? '';

            // CHANGE HERE
            if (deviceName === '') {
                if (settled) return;
                settled = true;
                clearTimeout(timeoutId)
                manager.stopDeviceScan()
                try {
                    const connected = await device.connect()
                    const readyDevice = await connected.discoverAllServicesAndCharacteristics()
                    connectedDevice = readyDevice
                    resolve(readyDevice)
                } catch (connectError) {
                    reject(connectError)
                }
            }
        })
    })
```
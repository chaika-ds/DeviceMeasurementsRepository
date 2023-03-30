# DeviceMeasurementsRepository
1. Run EatonTest - service with REST GET endpoint /v1/device/{id}, where id - the device type number in appsettings: "Devices": "Lamp, Valve, Transmission"
2. The devices measurements is keeping in resource file - DevicesMasurementsData.json
3. On statring project meddleware the measurements data from resource id is storing to InMemory table.
4. On GET request the last measurements from InMemory according to the device type is returning. If no data found for device, the "NotFound" code is returning.
6. Every success request is removing proper item from InMemory table.
7. In EatonUnitTest is an example of unit-integration test - GetDeviceData, where test check if controller  GetDeviceData returns result on InputId and removes this data from repository.

[USB_fomu_AND_feather.pcapng](https://github.com/ulx3s/ulx3s.github.io/raw/master/files/USB_fomu_AND_feather.pcapng) is a wireshark USB capture file to determine why fomu and Feather M0 don't play well together.

The first 52 packets get auto-populated when simply starting Wireshark. (mouse disconnected)

The subsequent packets show the interaction between the fomu and the Adafruit Feather M0, both plugged into a USB hub, when that hub is connected to the host.

See [discussion on twitter](https://twitter.com/tannewt/status/1234869391163981824?s=20)

![feather_device_detail_tab.png](./feather_device_detail_tab.png)
![feather_device_detail_tab.png](./feather_device_driver_tab.png)
![feather_device_detail_tab.png](./feather_device_events_tab.png)
![feather_device_detail_tab.png](./feather_device_general_tab.png)


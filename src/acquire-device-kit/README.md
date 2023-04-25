# Acquire Device Kit

This is a header only library. Some types are defined outside this library -
it needs to be combined with `acquire-device-properties` to be fully defined.

Acquire relies on device adapters to define video sources, filters and sinks.
The Device Kit defines the interfaces that need to be implemented to create a
device adapter.

Each device adapter is compiled to a shared library that exposes a single
function, `acquire_driver_init_v0()`. That function returns a "Driver"
instance. Here, a Driver's responsibility is to list a number of devices that
can be opened and to manage those devices as resources. It also manages those
resources.

The "Devices" themselves may implement specific interfaces depending on their
Kind. See `storage.h` and `camera.h` for details.


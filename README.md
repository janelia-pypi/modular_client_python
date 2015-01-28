modular_device_python
=====================

This Python package (modular\_device) creates a class named
ModularDevice, which contains an instance of
serial\_device2.SerialDevice and adds methods to it, like auto
discovery of available modular devices in Linux, Windows, and Mac OS
X. This class automatically creates methods from available functions
reported by the modular device when it is running the appropriate
firmware.

Authors:

    Peter Polidoro <polidorop@janelia.hhmi.org>

License:

    BSD

##Example Usage


```python
from modular_device import ModularDevice
dev = ModularDevice() # Automatically finds device if one available
dev = ModularDevice('/dev/ttyACM0') # Linux specific port
dev = ModularDevice('/dev/tty.usbmodem262471') # Mac OS X specific port
dev = ModularDevice('COM3') # Windows specific port
dev.get_device_info()
dev.get_methods()
devs = ModularDevices()  # Automatically finds all available devices
devs.items()
dev = devs[name][serial_number]
```

More Detailed Examples:

<https://github.com/JaneliaSciComp/modular_device_arduino>

##Installation

###Linux and Mac OS X

[Setup Python for Linux](./PYTHON_SETUP_LINUX.md)

[Setup Python for Mac OS X](./PYTHON_SETUP_MAC_OS_X.md)

```shell
mkdir -p ~/virtualenvs/modular_device
virtualenv ~/virtualenvs/modular_device
source ~/virtualenvs/modular_device/bin/activate
pip install modular_device
```

###Windows

[Setup Python for Windows](./PYTHON_SETUP_WINDOWS.md)

```shell
virtualenv C:\virtualenvs\modular_device
C:\virtualenvs\modular_device\Scripts\activate
pip install modular_device
```

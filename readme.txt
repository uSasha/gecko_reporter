Simple way to make external custom USB keyboard.
In this case it has two functions: 1 button copy and paste.
This example project uses the EFM32 USB Device protocol stack
and implements an USB HID class keyboard device. Also I implemented some fun graphics.

The HID device enumerates and immediately disables the Low Energy USB features
(which are enabled by default in the USB protocol stack), allowing observation
of "normal" power consumption on VBUS.

The example is power optimized when LEM is enabled.  With the STK power switch in
"USB" position (board power is drawn from USB host via VBUS), when USB cable is plugged
in and USB is active the current drawn from VBUS is ~8.3 mA in normal mode, or ~5.8 mA
when LEM is enabled, of which only ~460 uA is consumed by the USB PHY.  When the cable
is disconnected or the device is suspended, the current is less than 5 uA.


Board:  Silicon Labs SLSTK3400A Starter Kit
Device: EFM32HG322F64

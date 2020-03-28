# Hackintosh

crashlog


```
panic(cpu 0 caller 0xffffff800c0a2d1c): Sleep transition timed out after 180 seconds while calling power state change callbacks. Suspected bundle: com.apple.iokit.IOUSBHostFamily. Thread 0x12ee.
Failure code:: 0x00000040 00000014

Backtracing specified thread
Backtrace (CPU 0), Frame : Return Address
0xffffff83c5ac3900 : 0xffffff800ba60178 mach_kernel : _machine_switch_context + 0xc8
0xffffffa3dc85b9b0 : 0xffffff800b95d771 mach_kernel : _thread_unstop + 0x1771
0xffffffa3dc85ba20 : 0xffffff800b95bf6f mach_kernel : _thread_block_reason + 0xaf
0xffffffa3dc85ba70 : 0xffffff800b94cdd3 mach_kernel : _lck_mtx_sleep_deadline + 0x73
0xffffffa3dc85bab0 : 0xffffff800c03fb9f mach_kernel : __ZN10IOWorkLoop9sleepGateEPvyj + 0xbf
0xffffffa3dc85baf0 : 0xffffff800c040ca3 mach_kernel : __ZN13IOEventSource9sleepGateEPvyj + 0x53
0xffffffa3dc85bb30 : 0xffffff7f8ca98278 com.apple.iokit.IOUSBHostFamily : __ZN22AppleUSBHostController20lowerOnePowerStateToEm + 0x114
0xffffffa3dc85bca0 : 0xffffff7f8d1feaf4 com.apple.driver.usb.AppleUSBXHCI : __ZN12AppleUSBXHCI20lowerOnePowerStateToEm + 0x2e2
0xffffffa3dc85bd10 : 0xffffff7f8d320e1a com.apple.driver.usb.AppleUSBXHCIPCI : __ZN15AppleUSBXHCIPCI20lowerOnePowerStateToEm + 0x1fc
0xffffffa3dc85bd60 : 0xffffff7f8ca97073 com.apple.iokit.IOUSBHostFamily : __ZN22AppleUSBHostController18setPowerStateGatedEmP9IOService + 0x2db
0xffffffa3dc85bdc0 : 0xffffff800c042578 mach_kernel : __ZN13IOCommandGate9runActionEPFiP8OSObjectPvS2_S2_S2_ES2_S2_S2_S2_ + 0x138
0xffffffa3dc85be20 : 0xffffff7f8ca96d94 com.apple.iokit.IOUSBHostFamily : __ZN22AppleUSBHostController13setPowerStateEmP9IOService + 0x32
0xffffffa3dc85be30 : 0xffffff800c027534 mach_kernel : __ZN9IOService19driverSetPowerStateEv + 0x184
0xffffffa3dc85bea0 : 0xffffff800c02733a mach_kernel : __ZN9IOService15pmDriverCalloutEPS_ + 0x2a
0xffffffa3dc85bec0 : 0xffffff800b97d7e5 mach_kernel : _thread_call_delayed_timer + 0xea5
0xffffffa3dc85bf40 : 0xffffff800b97d311 mach_kernel : _thread_call_delayed_timer + 0x9d1
0xffffffa3dc85bfa0 : 0xffffff800b8e213e mach_kernel : _call_continuation + 0x2e
      Kernel Extensions in backtrace:
         com.apple.iokit.IOUSBHostFamily(1.2)[B7CF50DA-73BD-3233-B207-9036BCAD8E1A]@0xffffff7f8ca83000->0xffffff7f8cb7bfff
            dependency: com.apple.driver.AppleBusPowerController(1.0)[9DFFFA4B-7650-37DD-9892-09A64F1A0BC4]@0xffffff7f8ca69000
            dependency: com.apple.driver.usb.AppleUSBCommon(1.0)[D19CDA63-3A3D-3C02-AEA2-C061630D17A7]@0xffffff7f8ca71000
            dependency: com.apple.driver.AppleUSBHostMergeProperties(1.2)[2A37B852-2C0E-3B06-A0D9-B153DD653807]@0xffffff7f8ca7f000
         com.apple.driver.usb.AppleUSBXHCI(1.2)[4650C412-33F6-322C-A80A-150FC3DA1B18]@0xffffff7f8d1ea000->0xffffff7f8d241fff
            dependency: com.apple.iokit.IOACPIFamily(1.4)[3D78401B-5D2D-33BC-9E41-DD2164EA874D]@0xffffff7f8ca36000
            dependency: com.apple.iokit.IOUSBHostFamily(1.2)[B7CF50DA-73BD-3233-B207-9036BCAD8E1A]@0xffffff7f8ca83000
            dependency: com.apple.driver.usb.AppleUSBCommon(1.0)[D19CDA63-3A3D-3C02-AEA2-C061630D17A7]@0xffffff7f8ca71000
         com.apple.driver.usb.AppleUSBXHCIPCI(1.2)[71C22181-4BD4-3E9B-AD35-E10850981E3A]@0xffffff7f8d319000->0xffffff7f8d34afff
            dependency: com.apple.iokit.IOACPIFamily(1.4)[3D78401B-5D2D-33BC-9E41-DD2164EA874D]@0xffffff7f8ca36000
            dependency: com.apple.iokit.IOPCIFamily(2.9)[ADD485B5-3EF8-37C4-B3C5-F86326E497A4]@0xffffff7f8c32f000
            dependency: com.apple.iokit.IOUSBHostFamily(1.2)[B7CF50DA-73BD-3233-B207-9036BCAD8E1A]@0xffffff7f8ca83000
            dependency: com.apple.driver.usb.AppleUSBCommon(1.0)[D19CDA63-3A3D-3C02-AEA2-C061630D17A7]@0xffffff7f8ca71000
            dependency: com.apple.driver.usb.AppleUSBXHCI(1.2)[4650C412-33F6-322C-A80A-150FC3DA1B18]@0xffffff7f8d1ea000

BSD process name corresponding to current thread: kernel_task
Boot args: -v keepsyms=1 agdpmod=pikera alcid=1 

Mac OS version:
19D76

Kernel version:
Darwin Kernel Version 19.3.0: Thu Jan  9 20:58:23 PST 2020; root:xnu-6153.81.5~1/RELEASE_X86_64
Kernel UUID: A8DDE75C-CD97-3C37-B35D-1070CC50D2CE
Kernel slide:     0x000000000b600000
Kernel text base: 0xffffff800b800000
__HIB  text base: 0xffffff800b700000
System model name: iMacPro1,1 (Mac-7BA5B2D9E42DDD94)
System shutdown begun: NO
Panic diags file available: NO (0xe00002bc)

System uptime in nanoseconds: 872601815252
```

解决办法1：

https://github.com/khronokernel/Opencore-Vanilla-Desktop-Guide/blob/master/AMD/AMD-USB-map.md

解决办法2:
拔掉USB设备，按睡眠按钮



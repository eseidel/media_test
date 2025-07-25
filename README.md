# media_test

Reproduction for https://github.com/shorebirdtech/shorebird/issues/3243

Instructions:

`shorebird release android`
`shorebird preview`

Should crash on launch.

Crashes on devices and emulators with:

```
7-25 14:11:59.707  7521  7521 F DEBUG   : *** *** *** *** *** *** *** *** *** *** *** *** *** *** *** ***
07-25 14:11:59.707  7521  7521 F DEBUG   : Build fingerprint: 'google/sdk_gphone64_arm64/emulator64_arm64:12/SE1A.220630.001.A1/9056438:userdebug/dev-keys'
07-25 14:11:59.707  7521  7521 F DEBUG   : Revision: '0'
07-25 14:11:59.707  7521  7521 F DEBUG   : ABI: 'arm64'
07-25 14:11:59.708  7521  7521 F DEBUG   : Timestamp: 2025-07-25 14:11:59.607169109-0700
07-25 14:11:59.708  7521  7521 F DEBUG   : Process uptime: 0s
07-25 14:11:59.708  7521  7521 F DEBUG   : Cmdline: com.example.media_test
07-25 14:11:59.708  7521  7521 F DEBUG   : pid: 7480, tid: 7480, name: mple.media_test  >>> com.example.media_test <<<
07-25 14:11:59.708  7521  7521 F DEBUG   : uid: 10147
07-25 14:11:59.708  7521  7521 F DEBUG   : tagged_addr_ctrl: 0000000000000001
07-25 14:11:59.708  7521  7521 F DEBUG   : signal 7 (SIGBUS), code 1 (BUS_ADRALN), fault addr 0x2
07-25 14:11:59.708  7521  7521 F DEBUG   :     x0  b400007954dd3360  x1  00000077e8680b34  x2  b400007954dd3360  x3  b400007954dd3360
07-25 14:11:59.708  7521  7521 F DEBUG   :     x4  0000007600009da1  x5  00000076001a6a81  x6  00000076001acc91  x7  00000076001b7f01
07-25 14:11:59.708  7521  7521 F DEBUG   :     x8  0000000000000000  x9  00000077f546e010  x10 0000000000000001  x11 0000000000000000
07-25 14:11:59.708  7521  7521 F DEBUG   :     x12 0000000000000002  x13 ffffff89ff9d7ad7  x14 0000007fd01f76d8  x15 0000007fd01f7e70
07-25 14:11:59.708  7521  7521 F DEBUG   :     x16 00000077fecba198  x17 0000007b22f82bd8  x18 0000007b29d56000  x19 b400007954dd3410
07-25 14:11:59.708  7521  7521 F DEBUG   :     x20 00000077e8680b34  x21 b400007954dd3360  x22 b400007954dd3360  x23 b400007884ddf9f0
07-25 14:11:59.708  7521  7521 F DEBUG   :     x24 0000007600008081  x25 0000007fcfa29000  x26 b4000079c4dee2c0  x27 0000007600500080
07-25 14:11:59.708  7521  7521 F DEBUG   :     x28 0000000800000076  x29 0000007fd01f7e80
07-25 14:11:59.708  7521  7521 F DEBUG   :     lr  00000077e8690a9c  sp  0000007fd01f7e70  pc  0000000000000002  pst 0000000020001800
07-25 14:11:59.708  7521  7521 F DEBUG   : backtrace:
07-25 14:11:59.708  7521  7521 F DEBUG   :       #00 pc 0000000000000002  <unknown>
07-25 14:11:59.708  7521  7521 F DEBUG   :       #01 pc 0000000000010a98  [anon:FfiCallbackMetadata::TrampolinePage]
```
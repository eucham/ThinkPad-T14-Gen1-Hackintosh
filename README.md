## 笔记本型号

**ThinkPad T14 Gen1**，详细参数如下：

```shell
                    'c.          SB@ThinkPad-T14.lan
                 ,xNMM.          -----------------------
               .OMMMMo           OS: macOS 12.3.1 21E258 x86_64
               OMMM0,            Host: Hackintosh (SMBIOS: MacBookPro16,2)
     .;loddo:' loolloddol;.      Kernel: 21.4.0
   cKMMMMMMMMMMNWMMMMMMMMMM0:    Uptime: 1 hour, 53 mins
 .KMMMMMMMMMMMMMMMMMMMMMMMWd.    Packages: 31 (brew)
 XMMMMMMMMMMMMMMMMMMMMMMMX.      Shell: zsh 5.8
;MMMMMMMMMMMMMMMMMMMMMMMM:       Resolution: 1920x1080
:MMMMMMMMMMMMMMMMMMMMMMMM:       DE: Aqua
.MMMMMMMMMMMMMMMMMMMMMMMMX.      WM: Quartz Compositor
 kMMMMMMMMMMMMMMMMMMMMMMMMWd.    WM Theme: Blue (Light)
 .XMMMMMMMMMMMMMMMMMMMMMMMMMMk   Terminal: iTerm2
  .XMMMMMMMMMMMMMMMMMMMMMMMMK.   Terminal Font: Monaco 18
    kMMMMMMMMMMMMMMMMMMMMMMd     CPU: Intel i7-10510U (8) @ 1.80GHz
     ;KMMMMMMMWXXWMMMMMMMk.      GPU: Intel UHD Graphics 620
       .cooc,.    .,coo:.        Memory: 7221MiB / 16384MiB
```

## BISO Setting

- 进 BIOS：开机 -> `Enter` -> `F1`
- 进系统选择：开机 -> `Enter` -> `F12`

> 能设置的，尽量都设置上。

### 禁用清单

- `Fast Boot` - 快速启动
- `VT-d` (can be enabled if you set DisableIoMapper to YES) - VT-d（如果DisableIOMapper Quicks设置为YES，则可以启用）
- `CSM` - CSM 兼容性支持模块
- `Thunderbolt` - 雷雳
- `Intel SGX` - 英特尔SGX
- `Intel Platform Trust`- 英特尔平台信任
- `CFG Lock` (MSR 0xE2 write protection) - CFG锁（MSR 0xE2写保护）（必须关闭，如果找不到该选项，则在OpenCore的config-内核-> Quirks下启用与CFG Lock相关选项）
- `ecure Boot` - 安全启动
- `Parallel Port` - 并口
- `Serial/COM Port` - 串行/COM端口

### 启用

- `VT-x` - VT-x
- `UEFI Boot Mode` UEFI启动模式。请不要使用Legacy
- 硬盘模式：改为`AHCI`。不能用IDE和RST RAID。
- `Above 4G decoding` - 大于4G地址空间解码
- `Hyper-Threading` - 超线程
- `Execute Disable Bit` - 执行禁用位
- `EHCI/XHCI Hand-off` - EHCI / XHCI接手控制
- `OS type`: `Windows 8.1/10 UEFI Mode` - 操作系统类型：Windows 8.1 / 10 UEFI模式
- `DVMT Pre-Allocated`(iGPU Memory): DVMT预分配（iGPU内存）：`64MB`（如果能设Max就设）
- `Legacy RTC Device` - 传统RTC设备

### Reference

- [simongu20070911/thinkpad-t14-gen1-i7-10510U-hackintosh-efi](https://github.com/simongu20070911/thinkpad-t14-gen1-i7-10510U-hackintosh-efi)
- [soft98-top/Lenovo-ThinkPad-L14-Gen1-i7-10510u-Hackintosh](https://github.com/soft98-top/Lenovo-ThinkPad-L14-Gen1-i7-10510u-Hackintosh)
- [D9E0/lenovo-thinkpad-t14s-opencore](https://github.com/D9E0/lenovo-thinkpad-t14s-opencore)
- [Lenovo ThinkPad T14s Monterey 12.2 SUCCESS](https://www.reddit.com/r/hackintosh/comments/soq5ke/lenovo_thinkpad_t14s_monterey_122_success/)
- [【黑果小兵】macOS Monterey 12.5.1 21G83 Installer for OpenCore 0.8.4 and CLOVER 5148 and FirPE ](https://blog.daliansky.net/macOS-Monterey-12.5.1-21G83-Release-version-with-OC-0.8.4-CLOVER-5148-and-FirPE-original-image.html)
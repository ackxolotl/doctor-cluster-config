# martha.r

```
System:    Host: martha Kernel: 5.15.14 x86_64 bits: 64 compiler: gcc v: 10.3.0 Console: N/A 
           Distro: NixOS 21.11 (Porcupine) 
Machine:   Type: Desktop System: NOVATECH product: PC-BX19795 v: V1.0 serial: 7456935-002 Chassis: 
           type: 3 v: 1.0 serial: 7456935-002 
           Mobo: ASUSTeK model: PRIME Z390-P v: Rev X.0x serial: 190347447802077 
           UEFI: American Megatrends v: 2417 date: 06/03/2019 
Memory:    RAM: total: 62.54 GiB used: 17.55 GiB (28.1%) 
           Array-1: capacity: 64 GiB slots: 4 EC: None max-module-size: 16 GiB note: est. 
           Device-1: ChannelA-DIMM1 size: 16 GiB speed: 2666 MT/s type: DDR4 detail: synchronous 
           bus-width: 64 bits total: 64 bits manufacturer: Micron part-no: 16ATF2G64AZ-2G6E1 
           serial: 1E915F06 
           Device-2: ChannelA-DIMM2 size: 16 GiB speed: 2666 MT/s type: DDR4 detail: synchronous 
           bus-width: 64 bits total: 64 bits manufacturer: Micron part-no: 16ATF2G64AZ-2G6E1 
           serial: 1E915F22 
           Device-3: ChannelB-DIMM1 size: 16 GiB speed: 2666 MT/s type: DDR4 detail: synchronous 
           bus-width: 64 bits total: 64 bits manufacturer: Micron part-no: 16ATF2G64AZ-2G6E1 
           serial: 1E915EFC 
           Device-4: ChannelB-DIMM2 size: 16 GiB speed: 2666 MT/s type: DDR4 detail: synchronous 
           bus-width: 64 bits total: 64 bits manufacturer: Micron part-no: 16ATF2G64AZ-2G6E1 
           serial: 1E91605C 
PCI Slots: Slot: 0 type: x1 PCI Express <BAD INDEX> status: Available length: Short 
           Slot: 1 type: x16 PCI Express <BAD INDEX> status: In Use length: Long 
           Slot: 2 type: x1 PCI Express PCIEX1_2 status: Available length: Short 
           Slot: 3 type: x16 PCI Express PCIEX16_2 status: Available length: Long 
           Slot: 4 type: x1 PCI Express PCIEX1_3 status: Available length: Short 
           Slot: 5 type: x1 PCI Express PCIEX1_4 status: In Use length: Short 
CPU:       Info: 8-Core model: Intel Core i9-9900K bits: 64 type: MT MCP arch: Kaby Lake 
           note: check rev: C cache: L1: 512 KiB L2: 16 MiB L3: 16 MiB 
           flags: avx avx2 lm nx pae sse sse2 sse3 sse4_1 sse4_2 ssse3 vmx bogomips: 115200 
           Speed: 4800 MHz min/max: 800/5000 MHz volts: 0.9 V ext-clock: 100 MHz 
           Core speeds (MHz): 1: 4800 2: 4793 3: 4802 4: 4785 5: 4801 6: 4758 7: 4800 8: 4780 
           9: 4801 10: 4801 11: 4801 12: 4800 13: 4802 14: 4797 15: 4799 16: 4801 
Graphics:  Device-1: Intel CoffeeLake-S GT2 [UHD Graphics 630] vendor: ASUSTeK driver: i915 
           v: kernel bus-ID: 00:02.0 chip-ID: 8086:3e98 class-ID: 0300 
           Display: server: No display server data found. Headless machine? tty: N/A 
           Message: Unable to show advanced data. Required tool glxinfo missing. 
Audio:     Device-1: Intel Cannon Lake PCH cAVS vendor: ASUSTeK driver: snd_hda_intel v: kernel 
           bus-ID: 00:1f.3 chip-ID: 8086:a348 class-ID: 0403 
           Sound Server-1: ALSA v: k5.15.14 running: yes 
Network:   Device-1: Intel Ethernet XL710 for 40GbE QSFP+ driver: i40e v: kernel port: efa0 
           bus-ID: 01:00.0 chip-ID: 8086:1583 class-ID: 0200 
           IF: enp1s0f0 state: up speed: 40000 Mbps duplex: full mac: 3c:fd:fe:9e:97:58 
           IP v4: 192.168.161.142/24 type: dynamic scope: global 
           IP v6: fd9a:5371:cd3f:0:3efd:feff:fe9e:9758/64 type: dynamic mngtmpaddr noprefixroute 
           scope: global 
           IP v6: fe80::3efd:feff:fe9e:9758/64 scope: link 
           Device-2: Intel Ethernet XL710 for 40GbE QSFP+ driver: i40e v: kernel port: efa0 
           bus-ID: 01:00.1 chip-ID: 8086:1583 class-ID: 0200 
           IF: enp1s0f1 state: up speed: 40000 Mbps duplex: full mac: 3c:fd:fe:9e:97:59 
           IP v4: 192.168.161.80/24 type: dynamic scope: global 
           IP v6: fd9a:5371:cd3f:0:3efd:feff:fe9e:9759/64 type: dynamic mngtmpaddr noprefixroute 
           scope: global 
           IP v6: fe80::3efd:feff:fe9e:9759/64 scope: link 
           Device-3: Realtek RTL8111/8168/8411 PCI Express Gigabit Ethernet 
           vendor: ASUSTeK PRIME B450M-A driver: r8169 v: kernel port: 3000 bus-ID: 05:00.0 
           chip-ID: 10ec:8168 class-ID: 0200 
           IF: enp5s0 state: up speed: 1000 Mbps duplex: full mac: 04:d4:c4:04:4a:ba 
           IP v4: 129.215.165.53/23 type: dynamic scope: global 
           IP v6: 2001:630:3c1:164:6d4:c4ff:fe04:4aba/64 type: dynamic mngtmpaddr noprefixroute 
           scope: global 
           IP v6: fe80::6d4:c4ff:fe04:4aba/64 scope: link 
           IF-ID-1: docker0 state: down mac: 02:42:dd:21:89:e1 
           IP v4: 172.17.0.1/16 scope: global broadcast: 172.17.255.255 
           IF-ID-2: tinc.retiolum state: unknown speed: 10 Mbps duplex: full mac: N/A 
           IP v4: 10.243.29.179/12 scope: global broadcast: 10.255.255.255 
           IP v6: 42:0:3c46:5466:7dbe:f27a:673f:ea64/12 scope: global 
           IP v6: fe80::80d6:5c1a:258a:3e9/64 virtual: stable-privacy scope: link 
           WAN IP: 129.215.165.53 
RAID:      Device-1: zroot type: zfs status: ONLINE level: linear size: 888 GiB free: 571 GiB 
           allocated: 317 GiB 
           Components: Online: N/A 
Drives:    Local Storage: total: raw: 2.69 TiB usable: 3.56 TiB used: 293.46 GiB (8.1%) 
           ID-1: /dev/nvme0n1 vendor: Intel model: SSDPEDKE020T7 size: 1.82 TiB speed: 31.6 Gb/s 
           lanes: 4 rotation: SSD serial: PHLE844600FF2P0IGN rev: QDV101D1 
           ID-2: /dev/sda vendor: Kingston model: SA400S37960G size: 894.25 GiB speed: 6.0 Gb/s 
           rotation: SSD serial: 50026B7682C2E52B rev: 61F1 scheme: GPT 
Partition: ID-1: / size: 827.88 GiB used: 292.92 GiB (35.4%) fs: zfs logical: zroot/root/nixos 
           ID-2: /boot size: 499.7 MiB used: 385.8 MiB (77.2%) fs: vfat dev: /dev/sda1 
           ID-3: /tmp size: 535.11 GiB used: 160.8 MiB (0.0%) fs: zfs logical: zroot/root/tmp 
Swap:      Alert: No swap data was found. 
Sensors:   Missing: Required tool sensors not installed. Check --recommends 
Info:      Processes: 326 
           Uptime: 14:50:01  up 1 day  5:04,  1 user,  load average: 0.18, 0.07, 0.02 wakeups: 0 
           Init: systemd v: 249 target: multi-user.target Compilers: gcc: 10.3.0 Packages: 
           nix-sys: 470 Client: Sudo v: 1.9.7p2 inxi: 3.3.04 
```

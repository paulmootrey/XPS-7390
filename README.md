
# Welcome to my **Dell XPS 7390** repository running GentooLTO

 - Xanmod configuration 5.7.10-xanmod-x86_64 has all devices drivers and
   firmware built-in
   (https://xanmod.org/)
 - XPS BIOS v1.5.1 extracted using Dell_PFS_Extract
   (https://github.com/platomav/BIOSUtilities)
 - Management Engine bits cleaned using me_cleaner
   (https://github.com/corna/me_cleaner).

> BIOS is untested as I do not have a way to recover the machine if
> there is a failure during the flash. If someone is brave enough to
> test or has a way to rollback please contact me.

 - Repositories in use:
   lto-overlay  mv
   (https://github.com/InBetweenNames/gentooLTO)
   (https://cgit.gentoo.org/user/mv.git)

**me_cleaner output**:

'1 -- 2 Intel Management Engine Unmanaged Firmware Update v14.0.bin'

    ME/TXE image detected
    Found FPT header at 0x10
    Found 17 partition(s)
    Found FTPR header: FTPR partition spans from 0x2000 to 0x11b000
    Found FTPR manifest at 0x2238
    ME/TXE firmware version 14.0.11.1205 (generation 3)
    WARNING Unknown public key 8e4f834644da2bef03039d69d41ecf02
            Assuming Intel ME
            Please report this warning to the project's maintainer!
    Reading partitions list...
     PSVN (0x00001000 - 0x000001100, 0x00000100 total bytes): removed
     UEP  (      no data here      , 0x00000000 total bytes): nothing to remove
     FTPR (0x00002000 - 0x00011b000, 0x00119000 total bytes): NOT removed
     FTUP (      no data here      , 0x00000000 total bytes): nothing to remove
     DLMP (      no data here      , 0x00000000 total bytes): nothing to remove
     IVBP (0x0011b000 - 0x00011f000, 0x00004000 total bytes): removed
     MFS  (0x0011f000 - 0x000183000, 0x00064000 total bytes): removed
     NFTP (0x00183000 - 0x0002c8000, 0x00145000 total bytes): removed
     ROMB (      no data here      , 0x00000000 total bytes): nothing to remove
     UTOK (0x002c8000 - 0x0002ca000, 0x00002000 total bytes): removed
     HVMP (0x002ca000 - 0x0002ca00c, 0x0000000c total bytes): removed
     RBEP (0x002cb000 - 0x0002db000, 0x00010000 total bytes): removed
     RSTR (0x002db000 - 0x0002db018, 0x00000018 total bytes): removed
     FLOG (0x002dc000 - 0x0002dd000, 0x00001000 total bytes): removed
     IMDP (0x002dd000 - 0x0002dd040, 0x00000040 total bytes): removed
     PMCP (0x002de000 - 0x0002ef000, 0x00011000 total bytes): removed
     PCHC (0x002ef000 - 0x0002f0000, 0x00001000 total bytes): removed
    Removing partition entries in FPT...
    Removing EFFS presence flag...
    Correcting checksum (0xa5)...
    Reading FTPR modules list...
     FTPR.man     (uncompressed, 0x002238 - 0x003000): NOT removed, partition manif.
     rot.key      (LZMA/uncomp., 0x003000 - 0x0034c0): removed
     kernel       (Huffman     , 0x0034c0 - 0x0126c0): NOT removed, essential
     syslib       (Huffman     , 0x0126c0 - 0x026a40): NOT removed, essential
     bup          (Huffman     , 0x026a40 - 0x04c440): NOT removed, essential
     pm           (Huffman     , 0x04c440 - 0x04f100): removed
     vfs          (Huffman     , 0x04f100 - 0x0602c0): removed
     evtdisp      (Huffman     , 0x0602c0 - 0x062d80): removed
     loadmgr      (Huffman     , 0x062d80 - 0x067500): removed
     busdrv       (Huffman     , 0x067500 - 0x069b80): removed
     gpio         (Huffman     , 0x069b80 - 0x06b6c0): removed
     ipc_drv      (Huffman     , 0x06b6c0 - 0x06dc80): removed
     prtc         (Huffman     , 0x06dc80 - 0x06ebc0): removed
     policy       (Huffman     , 0x06ebc0 - 0x074480): removed
     crypto       (Huffman     , 0x074480 - 0x09fd80): removed
     heci         (Huffman     , 0x09fd80 - 0x0a64c0): removed
     storage      (Huffman     , 0x0a64c0 - 0x0af8c0): removed
     pmdrv        (Huffman     , 0x0af8c0 - 0x0b1b80): removed
     maestro      (Huffman     , 0x0b1b80 - 0x0b4480): removed
     fpf          (Huffman     , 0x0b4480 - 0x0b7e00): removed
     fwupdate     (Huffman     , 0x0b7e00 - 0x0bda00): removed
     ptt          (Huffman     , 0x0bda00 - 0x0ddb40): removed
     touch_fw     (Huffman     , 0x0ddb40 - 0x11b000): removed
    The ME minimum size should be 331776 bytes (0x51000 bytes)
    Checking the FTPR RSA signature... VALID
    Done! Good luck!`


**lspci -k output**:

    00:00.0 Host bridge: Intel Corporation Device 9b51
    	Subsystem: Dell Device 0962
    00:02.0 VGA compatible controller: Intel Corporation Device 9bca (rev 04)
    	DeviceName: To Be Filled by O.E.M.
    	Subsystem: Dell Device 0962
    	Kernel driver in use: i915
    00:04.0 Signal processing controller: Intel Corporation Xeon E3-1200 v5/E3-1500 v5/6th Gen Core Processor Thermal Subsystem
    	Subsystem: Dell Xeon E3-1200 v5/E3-1500 v5/6th Gen Core Processor Thermal Subsystem
    	Kernel driver in use: proc_thermal
    00:08.0 System peripheral: Intel Corporation Xeon E3-1200 v5/v6 / E3-1500 v5 / 6th/7th/8th Gen Core Processor Gaussian Mixture Model
    	Subsystem: Dell Xeon E3-1200 v5/v6 / E3-1500 v5 / 6th/7th/8th Gen Core Processor Gaussian Mixture Model
    00:12.0 Signal processing controller: Intel Corporation Comet Lake Thermal Subsytem
    	Subsystem: Dell Comet Lake Thermal Subsytem
    00:14.0 USB controller: Intel Corporation Device 02ed
    	Subsystem: Dell Device 0962
    	Kernel driver in use: xhci_hcd
    00:14.2 RAM memory: Intel Corporation Device 02ef
    	Subsystem: Dell Device 0962
    00:15.0 Serial bus controller [0c80]: Intel Corporation Serial IO I2C Host Controller
    	Subsystem: Dell Serial IO I2C Host Controller
    	Kernel driver in use: intel-lpss
    00:15.1 Serial bus controller [0c80]: Intel Corporation Device 02e9
    	Subsystem: Dell Device 0962
    	Kernel driver in use: intel-lpss
    00:16.0 Communication controller: Intel Corporation Comet Lake Management Engine Interface
    	Subsystem: Dell Comet Lake Management Engine Interface
    	Kernel driver in use: mei_me
    00:1c.0 PCI bridge: Intel Corporation Device 02bc (rev f0)
    	Kernel driver in use: pcieport
    00:1c.6 PCI bridge: Intel Corporation Device 02be (rev f0)
    	Kernel driver in use: pcieport
    00:1d.0 PCI bridge: Intel Corporation Device 02b0 (rev f0)
    	Kernel driver in use: pcieport
    00:1d.4 PCI bridge: Intel Corporation Device 02b4 (rev f0)
    	Kernel driver in use: pcieport
    00:1f.0 ISA bridge: Intel Corporation Device 0284
    	Subsystem: Dell Device 0962
    00:1f.3 Audio device: Intel Corporation Device 02c8
    	Subsystem: Dell Device 0962
    	Kernel driver in use: snd_hda_intel
    00:1f.4 SMBus: Intel Corporation Device 02a3
    	Subsystem: Dell Device 0962
    	Kernel driver in use: i801_smbus
    00:1f.5 Serial bus controller [0c80]: Intel Corporation Comet Lake SPI (flash) Controller
    	Subsystem: Dell Comet Lake SPI (flash) Controller
    01:00.0 Unassigned class [ff00]: Realtek Semiconductor Co., Ltd. RTS525A PCI Express Card Reader (rev 01)
    	Subsystem: Dell RTS525A PCI Express Card Reader
    	Kernel driver in use: rtsx_pci
    02:00.0 Network controller: Intel Corporation Wi-Fi 6 AX200 (rev 1a)
    	Subsystem: Bigfoot Networks, Inc. Wi-Fi 6 AX200
    	Kernel driver in use: iwlwifi
    03:00.0 PCI bridge: Intel Corporation JHL6540 Thunderbolt 3 Bridge (C step) [Alpine Ridge 4C 2016] (rev 02)
    	Kernel driver in use: pcieport
    04:00.0 PCI bridge: Intel Corporation JHL6540 Thunderbolt 3 Bridge (C step) [Alpine Ridge 4C 2016] (rev 02)
    	Kernel driver in use: pcieport
    04:01.0 PCI bridge: Intel Corporation JHL6540 Thunderbolt 3 Bridge (C step) [Alpine Ridge 4C 2016] (rev 02)
    	Kernel driver in use: pcieport
    04:02.0 PCI bridge: Intel Corporation JHL6540 Thunderbolt 3 Bridge (C step) [Alpine Ridge 4C 2016] (rev 02)
    	Kernel driver in use: pcieport
    04:04.0 PCI bridge: Intel Corporation JHL6540 Thunderbolt 3 Bridge (C step) [Alpine Ridge 4C 2016] (rev 02)
    	Kernel driver in use: pcieport
    05:00.0 System peripheral: Intel Corporation JHL6540 Thunderbolt 3 NHI (C step) [Alpine Ridge 4C 2016] (rev 02)
    	Subsystem: Dell JHL6540 Thunderbolt 3 NHI (C step) [Alpine Ridge 4C 2016]
    	Kernel driver in use: thunderbolt
    3b:00.0 USB controller: Intel Corporation JHL6540 Thunderbolt 3 USB Controller (C step) [Alpine Ridge 4C 2016] (rev 02)
    	Subsystem: Dell JHL6540 Thunderbolt 3 USB Controller (C step) [Alpine Ridge 4C 2016]
    	Kernel driver in use: xhci_hcd
    71:00.0 Non-Volatile memory controller: Lite-On Technology Corporation Device 2f00 (rev 01)
    	Subsystem: Marvell Technology Group Ltd. Device 1093
    	Kernel driver in use: nvme`

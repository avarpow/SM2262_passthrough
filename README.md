# Kernel patch for workaround MSI-X bug in the Silicon Motion SM2262 SSD Controller
 
* From: Alex Williamson <alex.williamson@redhat.com>

* Bugzilla and discussion https://bugzilla.kernel.org/show_bug.cgi?id=202055

Modified offsets and tested on Linux 5.7.10.

Fix bug when PCI passthrough:

 ```failed to add PCI capability 0x11[0x50]@0xb0: table & pba overlap, or they don't fit in BARs, or don't align.```

灵车硬盘aigo p2000 是SM2263主控，一样直通错误，此处已添加sm2263支持

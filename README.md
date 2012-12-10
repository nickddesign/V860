V860
====

ALCATEL V860_VODAFONE SMART II



Cygwin

cd /boot

./unpack-bootimg.pl boot.img


Subroutine Cwd::cwd redefined at /usr/lib/perl5/5.14/i686-cygwin-threads-64int/C                                                                                                    wd.pm line 407.
Subroutine Cwd::fastcwd redefined at /usr/lib/perl5/5.14/i686-cygwin-threads-64i                                                                                                    nt/Cwd.pm line 819.
Name "DynaLoader::CARP_NOT" used only once: possible typo at /usr/lib/perl5/5.14                                                                                                    /Carp.pm line 345.
Name "Cwd::CARP_NOT" used only once: possible typo at /usr/lib/perl5/5.14/Carp.p                                                                                                    m line 345.
Name "File::Path::CARP_NOT" used only once: possible typo at /usr/lib/perl5/5.14                                                                                                    /Carp.pm line 345.
Name "Exporter::CARP_NOT" used only once: possible typo at /usr/lib/perl5/5.14/C                                                                                                    arp.pm line 345.

kernel written to boot.img-kernel.gz
ramdisk written to boot.img-ramdisk.cpio.gz
2350 blocks

extracted ramdisk contents to directory boot.img-ramdisk/

$ gunzip -c ../boot.img-ramdisk.cpio | cpio -i

gzip: ../boot.img-ramdisk.cpio.gz: decompression OK, trailing garbage ignored
511 blocks

$ find . | cpio -o -H newc | gzip > ../newramdisk.cpio.gz
511 blocks

---------------------------------------------------------------------------------
              Tct  Recovery 4 options


$ ./unpack-bootimg.pl recovery.img
Subroutine Cwd::cwd redefined at /usr/lib/perl5/5.14/i686-cygwin-threads-64int/Cwd.pm line 407.
Subroutine Cwd::fastcwd redefined at /usr/lib/perl5/5.14/i686-cygwin-threads-64int/Cwd.pm line 819.
Name "DynaLoader::CARP_NOT" used only once: possible typo at /usr/lib/perl5/5.14/Carp.pm line 345.
Name "Cwd::CARP_NOT" used only once: possible typo at /usr/lib/perl5/5.14/Carp.pm line 345.
Name "File::Path::CARP_NOT" used only once: possible typo at /usr/lib/perl5/5.14/Carp.pm line 345.
Name "Exporter::CARP_NOT" used only once: possible typo at /usr/lib/perl5/5.14/Carp.pm line 345.

kernel written to recovery.img-kernel.gz
ramdisk written to recovery.img-ramdisk.cpio.gz

gzip: ../recovery.img-ramdisk.cpio.gz: decompression OK, trailing garbage ignored
4276 blocks

extracted ramdisk contents to directory recovery.img-ramdisk/


               Recovery.fstab
               
# mount         fstype          device                  [device2]   [fstype2]   [fsoptions]         [fsoptions2]
/data           ext4            /dev/block/stl19        NULL        rfs         NULL                check=no
/sdcard         vfat            /dev/block/mmcblk0p1 
/system         ext4            /dev/block/stl15        NULL        rfs         NULL                check=no
/cache          ext4            /dev/block/stl16        NULL        rfs         NULL                check=no     
/custpack       ext4            /dev/block/stl18
/misc           mtd             /dev/block/stl13
/boot           mtd             /dev/block/stl11
/recovery       mtd             /dev/block/stl12
/modem          mtd             /dev/block/stl0
/bootloader     mtd             /dev/block/stl5
/sysparm_ind    mtd             /dev/block/stl1
/comms          mtd             /dev/block/stl2
/dsp_pram       mtd             /dev/block/stl3
/dsp_dram       mtd             /dev/block/stl4
/FOTAFLAG       mtd             /dev/block/stl10
/bootloader2    mtd             /dev/block/stl9



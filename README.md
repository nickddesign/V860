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




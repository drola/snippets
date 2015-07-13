VirtualBox
==========

Clone VDI
---------

    vboxmanage clonehd                                                              
    Usage:

    VBoxManage clonehd          <uuid|inputfile> <uuid|outputfile>
                                [--format VDI|VMDK|VHD|RAW|<other>]
                                [--variant Standard,Fixed,Split2G,Stream,ESX]
                                [--existing]


Example:

    vboxmanage clonehd ./original.vdi ./new.vdi


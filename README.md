============================================
Ceph-Dokan
============================================

CephFS Client on Win32 based on Dokany 0.7.4


Introduction
-----------

This program is based on original Ceph code and modifid for Win64 Platform.

It is compiled by gcc/g++, so it is native Win64 program.


How to use
------------

First install Dokany 0.7.4 on your Windows.

Now you can use ceph-dokan on your Windows and get full speed access to CephFS without slowly Samba.

    ceph-dokan.exe
     -c CephConf  (ex. /r c:\ceph.conf)
     -l DriveLetter (ex. /l m)

Example:  ceph-dokan.exe -c ceph.conf -l m

Then you will see a new Drive[M:] in your explorer.


How to compile
------------

Download & install minGW-w64 (gcc 7.2.0, x86_64 version)

Download Boost Libs in D:\boost_1_66_0

Compile boost system if you want (libboost_system-mgw72-mt-x64-1_66.a precompiled in repo, no need to compile):

bootstrap.bat gcc

b2 toolset=gcc --with-system

Then you will get libboost_system-mgw72-mt-x64-1_66.a in stage\lib of your boost directory.

Git clone the ceph-dokan, open cmd and cd ceph-dokan code directory, just input the command 'mingw32-make', after serval minutes you will get ceph-dokan.exe and libcephfs.dll.


Future
-----------
Ceph-Dokan will get continuous improvement and upgrade with upstream Ceph code.


+++
title = "Troubleshooting VirtualBox"
slug = "troubleshooting-virtualbox"
date = 2019-08-24
+++

# Summary

In a majority of the classes I’ve taught, there’s a strong dependence on virtualization. This initially makes sense from a **BYOD** (bring your own device) strategy, but can present some challenges. The first thing you will need to do is to navigate to the [Downloads](https://www.virtualbox.org/wiki/Downloads) page and pull the recent version.

## Extension Pack

This is an optional package that you can install that will enable your VirtualBox. You do not have to install this, unless I say otherwise. It allows you to do the following:

- Support for USB 2.0 and USB 3.0 Devices
- VirtualBox RDP
- Disk Encryption
- NVMe and PXE Boot

## Common Issues

I’ve encountered a large number of issues that students have experienced over time. Please ensure you’ve checked through each one of these items before coming to me in-class.

There are many cryptic errors that VirtualBox can throw. I’ll try to cover some examples. If all else fails, _Google it_.

## Enabling Virtualization

The most common problem I see is that the student does not have virtualization enabled in their PC.
You will need to enter the BIOS or UEFI in your computer during the boot up process (before the operating system starts).

Check your laptop model online to see what _key combination_ is needed during the boot process to access the computer settings.

When you get into the BIOS/UEFI settings, confirm that _virtualization_ is enabled. Sometimes this can be labeled as `VT-X` or `AMD-V` (depending on you CPU manufacturer).

## I/O or Disk Error

- Check to see if the virtual disk exists in the path that is configured.
- Check to see if your virtual machine’s virtual disk is out of space.
- Check to see if your system is out of disk space, especially if you’re using a dynamically growing virtual disk.
- Check to see if your system’s disk is healthy. If you’re using a SSD, you might be out of reads/writes.

## Register Error

Check to see if you already have a VM profile that’s already using that virtual disk.

## Extension Pack

- If you’re failing to install the Extension Pack, confirm that it is the same virtual as the VirtualBox you have installed.
- If you’re seeing **VERR ALREADY EXISTS**, you probably already have the Extension Pack installed.
- If you’re importing an existing VM profile that uses Extension Pack features, you will need to install the Extension Pack.
- You can create a new VM profile, using the existing virtual disk to work-around this.
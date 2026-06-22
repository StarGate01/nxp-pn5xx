# nxp-pn5xx
This is a fork of NXP's NFC Open Source Kernel mode driver that adds support for ACPI. Linux kernel **>= 3.17** is required.

As of mid-2018, many ThinkPad models include the NXP NPC300 chip for NFC. Although valid ACPI information is made available, the official driver does unfortunately not make use of it so the device does not work.

Currently, this fork only supports the bare minimum of configuration to make the NFC chip work (IRQ pin and VEN pin). I tested it on a Thinkpad T480s running Ubuntu 18.04 with kernel 4.15. According to reports, at the very least the T470 and Carbon X1C should also be supported. However, this is still an unofficial modification so USE AT YOUR OWN RISK. If the GPIO pins are configured wrong, you can potentially damage other components attached to them.

### Known issues
On my device, the touchpad becomes slow and unprecise as soon as I use the NFC chip. If anyone has any ideas what could be causing this and how to fix it, please open an issue.

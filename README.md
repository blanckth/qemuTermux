# [qemuTermux](https://github.com/blanckth/qemuTermux/)
Use QEMU in Termux as a full virtual machine and Deploy Any architecture OS and img and run without ROOT.
> ### Authur : **`Salar Muhammadi`**.
###### DOWNLOAD [Termux App](https://f-droid.org/en/packages/com.termux/) and install it , Run and Copy this command and run :
```bash
apt-get update -y && \
apt-get dist-upgrade -y && \
apt-get install qemu* -y && \
mkdir image && \
cd image;
```
> ###### Be Patience...
#### For Creating Virtual Machine HDD image do :
```bash
qemu-img create -f qcow2 hdd.img 10G
```
#### For Deploy And Running image :
```bash
qemu-system-x86_64 -smp 2 -net nic -net user -device AC97 -m 2048 -vnc 127.0.0.1:8 -cdrom image.iso -hda hdd.img
```
##### Now you can reach the Desktop with a VNC app like [AVNC](https://f-droid.org/en/packages/com.gaurav.avnc/) at localhost:5908
> #### For more Detail Options do :
```bash
qemu-system-x86_64 -h
```
#### Enjoy!

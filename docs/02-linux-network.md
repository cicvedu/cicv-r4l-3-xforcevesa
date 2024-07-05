# Build Linux Bootable Image & Setup Network

## Step 0: Setup Environment

Before doing this you should have done everything in [this section](./01-busybox-kernel.md) and have entered the Ubuntu environment.

## Step 1: Install Dependencies

```bash
sudo apt-get update
sudo apt-get install -y cpio
```

## Step 2: Build Linux Bootable Image & Bootstrap

```bash
cd src_e1000
bash build_image.sh
```

## Step 3: Configure Network

After entering the QEMU Linux tty, do this:

```bash
insmod r4l_e1000_demo.ko
ip link set eth0 up
ip addr add broadcast 10.0.2.255 dev eth0
ip addr add 10.0.2.15/255.255.255.0 dev eth0 
ip route add default via 10.0.2.1
ping 10.0.2.2
```

If you see ping responses, then you have successfully configured the network.

## Step 4: Exit QEMU

You can exit the QEMU Linux tty by pressing `Ctrl-A X`.

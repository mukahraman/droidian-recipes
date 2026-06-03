# Droidian — Samsung Galaxy Tab S7+ Wi-Fi (SM-T970)

[Droidian](https://droidian.org) is a Debian-based GNU/Linux mobile OS (Halium + Phosh) that runs on
Android hardware. This repository is the **image recipe** for the community port to the **Samsung
Galaxy Tab S7+ Wi-Fi** (`gts7xlwifi`) — its CI builds the flashable Droidian rootfs.

## Install

📖 **Full step-by-step install guide → [mukahraman/galaxy-tab-s7-plus-droidian](https://github.com/mukahraman/galaxy-tab-s7-plus-droidian)**
— from stock Android to a working Droidian: what works, the flashing tools, and every step.

📦 **Flashable rootfs image → [Releases → `nightly`](https://github.com/mukahraman/droidian-recipes/releases/tag/nightly)**
— the `droidian-*-gts7xlwifi-*.zip`.

> ⚠️ This is a **Samsung** device: its bootloader has **no fastboot**, so the generic Droidian
> `flash_all.sh` does **not** work here. You flash with **Heimdall** from Download Mode, and the kernel
> `boot.img` must first be wrapped for Samsung's ABL. The install guide above covers all of it — don't
> follow generic fastboot instructions.

## Building from source

This repo plugs into Droidian's image builder to produce the rootfs; CI publishes the result to
Releases. The kernel and device adaptation live in their own repos:

- [`kernel_samsung_sm8250`](https://github.com/mukahraman/kernel_samsung_sm8250) — kernel (`linux-bootimage-*.deb` + apt repo)
- [`adaptation-samsung-gts7xlwifi`](https://github.com/mukahraman/adaptation-samsung-gts7xlwifi) — device adaptation package

---
*Community port; not affiliated with Samsung or Droidian.*

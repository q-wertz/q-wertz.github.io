---
title: "Installation of Linux (Kubuntu) on Acer Aspire E15"
---

## Introduction

Installation of Linux (Kubuntu 24.04) on the Acer Aspire E15 was quite annoying.

Usual installation resulted in a `No bootable device` message during boot.


## Laptop

| Key          | Value        |
| ------------ | ------------ |
| Manufacturer | Acer         |
| Model        | Aspire E15   |
| Modelnumber  | E5-574G-56U6 |
| SNID         | 60303163175  |

- The original internal 1TB HDD was replaced with a 500GB SSD.


## HowTo

- Prepare a bootable USB stick with Linux distribution of choice (in my case I used Kubuntu 24.04)
- Make sure the SSD is has a GPT partition table (use LiveBoot if not and adapt)
    (Not sure whether the flags ?`boot`? and `grub_?` are required.)
- In BIOS (press `F2` during start)
    - Set an administrator password under `Security > Set Supervisor Password` (so that more settings can be adjusted)
    - Optional: Under `Security` select `Erase all Secure Boot Settings`
    - Disable `Secure Boot` (but keep `Boot Mode`: `UEFI`)
    - Make sure `Main > F12 Boot Menu` is enabled so that booting from external devices using `F12` is possible
- Reboot and interrupt boot using `F12`
- Select the prepared Linux boot stick and go through the installation procedure. 
    (Make sure you see `GPT` in the disc setup interface)
- After the installation boot to BIOS (pressing `F2`)
- Enable `Secure Boot` again
- Under `Security > Select an UEFI file as trusted for executing` select `HDD0 > EFI > UBUNTU > shimx64.efi` (not sure if the others also work) 
- Booting to the new system should now be possible


## More info

Much of the description is derived from the [Acer Forum](https://community.acer.com/en/discussion/643571/installing-linux-mint-aspire-e15) where also a side-by-side installation with Windows is described.
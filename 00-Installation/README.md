- Downloads: https://archlinux.org/download/
- Write file .ISO to USB Boot
- Select the first option, waiting a little, you will see lile the image below

![image](https://github.com/lcaohoanq/i-use-arch-btw/assets/136492579/52c7e8a6-f767-4b82-b9fd-635a8311776a)

- Test network connection `ping google.com`, im using the VM now so the network connected with my real machine,
if this is your first OS installation, there a solution (of course :D)

![image](https://github.com/lcaohoanq/i-use-arch-btw/assets/136492579/7018e154-8ea5-41cb-8612-51d436cc742b)

```bash
iwctl
devide list
station wlan0 get-networks
station wlan0 connect <Name>
#Passphrase: <Password>
```
- After that, `exit` and do the `ping` command again, it will work

```bash
pacman -Syy
```
![image](https://github.com/lcaohoanq/i-use-arch-btw/assets/136492579/30636095-7a74-4cce-a7be-b3b846dc5f41)

```bash
pacman -S archlinux-keyring
```

![image](https://github.com/lcaohoanq/i-use-arch-btw/assets/136492579/b1941dda-4911-49af-9a8b-36eb98a86115)


```bash
pacman -Sy archinstall
```

![image](https://github.com/lcaohoanq/i-use-arch-btw/assets/136492579/7a9a1072-73b6-4d3b-a733-74ba4c884128)


```bash
archinstall
```

![image](https://github.com/lcaohoanq/i-use-arch-btw/assets/136492579/60cc5c80-7bb7-44c3-a869-c667ddb81de3)

- Options
  - Archinstall language: English
  - Mirrors -> Mirrors Regions -> Vietnam (My Country)
  - Locales -> us
  - Disk configuration -> Use a best-effort default partion layout -> brtfs -> next next next
  - Bootloader -> Grub
  - Unified kernel images
  - Swap -> true
  - Hostname -> archlinux
  - Root password -> 
  - User account -> 
  - Profile -> Type: Minimal (for the installation Hyprland later)
  - Audio -> Pipewire
  - Kernels -> linux
  - Additional packages -> git neovim fastfetch curl nano btop fzf wget  
  - Network configuration -> Use NetworkManager
  - Timezone -> Asia/HoChiMinh
  - Automatic time sync (NTP) -> True
  - Optional repositories -> multilib
- Save and Install
- Enter
- 5....4....3...2...1

- Would you like to chroot into the newly created installation and perform post-installation configuration?
  - No
  - sudo reboot
 
- Login
- ping google.com for testig the network connection again

- git clone https://github.com/prasanthrangan/hyprdots.git
- cd hyprdots/Scripts/
- chmod +x ./install.sh
- ./install.sh

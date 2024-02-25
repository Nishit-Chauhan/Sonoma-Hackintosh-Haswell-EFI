# Sonoma-Hackintosh-Haswell-EFI

# Intel Core i5-4670 - Sonoma Hackintosh EFI (Opencore 0.9.6)
## Configuration

| Specifications | Details                                                  |
| ------------------- | ------------------------------------------- |
| MotherBoard     | Intel Original DH87MC      					|
| Processor           | Intel Core i5-4670 Processor    		    |
| Graphics | Intel HD 4600 (https://github.com/dortania/OpenCore-Legacy-Patcher/)              |
| Audio          | Realtek ALC892 audio (ALCID=1)            |
| Boot-Args | -v keepsyms=1 debug=0x100 alcid=1 amfi_get_out_of_my_way=0x1 ipc_control_port_options=0 |
| SMBIOS | MacPro7,1 (required RestrictEvents.kext) or iMac19,1 |

## Note
- amfi_get_out_of_my_way=0x1 - Add To fix Haswell graphics fix using OCLP
- ipc_control_port_options=0 - Add to fix crashing issue of some apps(Skype, Whatsapp, Spotify, etc)

## Disable SIP follow below steps before run OCLP (If OCLP complains about SIP)
 - sudo spctl --master-disable 
 - restart, on recovery, choose ultility, terminal add:
 - csrutil disable
 - csrutil authenticated-root disable
 - restart
 - Run opencore legacy patcher
   
## MacPro7,1
![screenshot](https://github.com/Nishit-Chauhan/Sonoma-Hackintosh-Haswell-EFI/assets/45855322/68bb6165-9d1b-4967-a6a2-846abf4ab6a1)

## iMac19,1
![Screenshot 2023-11-19 at 9 50 02 AM](https://github.com/Nishit-Chauhan/Sonoma-Hackintosh-Haswell-EFI/assets/45855322/d71ba6e1-22b8-408c-8215-baa9732869b7)

## Improvements
- This version was prepared using OpenCore 0.9.6 for MacOS Sonoma.

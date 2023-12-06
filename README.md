# ESP Tool firmware READ and WRITE


```cmd
esptool.exe --chip esp32 --port COM3 --baud 921600 --before default_reset --after hard_reset write_flash -z --flash_mode dio --flash_freq 80m --flash_size 4MB 0x1000
```


## Read Flash Memory:
```cmd
esptool.exe --port COM3 --baud 921600 flash_id
```


## Read Bin File:

> - Flash Size 4MB: 0x400000
>  - Flash Size 8MB: 0x800000
> - Flash Size 16MB: 0x1000000


```cmd
esptool.exe --port COM3 --baud 921600 read_flash 0 0x400000 readfirmware.bin
```


## Write Bin File:
```cmd
esptool.exe --chip esp32 --port COM3 --baud 921600 --before default_reset --after hard_reset write_flash -z --flash_mode dio --flash_freq 80m --flash_size 4MB 0x0 D:\newfirmware.bin
```

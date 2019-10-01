# Custom boot loader
This is a custom boot loader for RZ/A2M. By using the custom boot loader, you can drag & drop the ".bin" file to write the program.  

## Latest revision
revision 2

## How to use a custom boot loader
Add ``target.bootloader_img`` and ``target.app_offset`` to your project's ``mbed_app.json`` file as below.    
```
{
  ==== omit ====
    "target_overrides": {
      ==== omit ====
        "RZ_A2M_EVB": {
            "target.bootloader_img" : "bootloader_d_n_d/RZ_A2M_EVB_boot.bin",
            "target.app_offset"     : "0x40000",
            === omit ===
        },
        "RZ_A2M_EVB_HF": {
            "target.bootloader_img" : "bootloader_d_n_d/RZ_A2M_EVB_HF_boot.bin",
            "target.app_offset"     : "0x40000",
            === omit ===
        },
        "RZ_A2M_SBEV": {
            "target.bootloader_img" : "bootloader_d_n_d/RZ_A2M_SBEV_boot.bin",
            "target.app_offset"     : "0x40000",
            === omit ===
        },
        "SEMB1402": {
            "target.bootloader_img" : "bootloader_d_n_d/SEMB1402_boot.bin",
            "target.app_offset"     : "0x40000",
            === omit ===
        }
    }
}
```

Build the program. Two files ``xxxx.bin`` and ``xxxx_application.bin`` are created.  

1. Hold down ``SW3`` and press the reset button. (Or turn on the power.)  
2. Connect the USB cable to the PC, you can find the ``MBED`` directory.  
3. Drag & drop ``xxxx_application.bin`` to the ``MBED`` directory.  
4. When writing is completed, press the reset button.  

**Attention!**  
For the first time only, you need to write a custom bootloader as following.  

Download [e2studio 7.4.0 or lator](https://www.renesas.com/eu/en/products/software-tools/tools/ide/e2studio.html), and install. (Debugger : J-Link Base)  
Connect the J-Link to your board.  

![](docs/img/how_to_write_1.png)  
![](docs/img/how_to_write_2.png)  
![](docs/img/how_to_write_3.png)  
![](docs/img/how_to_write_4.png)  
![](docs/img/how_to_write_5.png)  
![](docs/img/how_to_write_6.png)  

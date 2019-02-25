# Custom boot loader
This is a custom boot loader for RZ/A2M. By using the custom boot loader, you can drag & drop the .bin file to write the program.  
Add ``target.bootloader_img`` and ``target.app_offset`` to your ``mbed_app.json`` file as below.  
```
{
    "config": {
        === omit ===
    },
    "target_overrides": {
        "*": {
            === omit ===
        },
        "RZ_A2M_EVB": {
            "target.bootloader_img" : "bootloader_d_n_d/RZ_A2M_EVB_boot.bin",
            "target.app_offset"     : "0x20000",
            === omit ===
        },
        "RZ_A2M_SBEV": {
            "target.bootloader_img" : "bootloader_d_n_d/RZ_A2M_SBEV_boot.bin",
            "target.app_offset"     : "0x20000",
            === omit ===
        },
        "SEMB1402": {
            "target.bootloader_img" : "bootloader_d_n_d/SEMB1402_boot.bin",
            "target.app_offset"     : "0x20000",
            === omit ===
        }
    }
}
```

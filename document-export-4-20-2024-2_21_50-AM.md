# 1. Embedded Linux Fundamentals



### **Linux Archiecture.**
- init-process.
- C-Library.
- userspace applications.
- Kernel.
- Drivers.
- **Code repo**: `﻿[﻿github.com/torvalds/linux](https://github.com/torvalds/linux)` 
---

### **1. Bootloader**.
Three types:

1. BIOS ---> Basic Input output system.
2. Secondary **Boot-loader** ---> Hardware specific code.
3. Custom **Boot-loader**.


## **Focusing on** `﻿Custom boot-loader .. ` 
Boot-loader ---> C/S:

1. Types.
2. Functions based on type.
3. Hardware support.


### **Types (Functions):**
1. Loader ---> init Hardware --> trigger next stage.
2. Loader + Monitors --->  
    1. monitor --> boot-loader provide interface for user-interactions [ex. Configurations  ... ].
3. Boot-loader has function specific code.


### **Custom Boot-loader types (Implementation):**
| Name | Description | Monitor | Arch. support | supported by yocto |
| ----- | ----- | ----- | ----- | ----- |
| U-Boot | Universal boot-loader | yes | ARM, x86 | yes |
| Red-Boot | Red-boot | yes | ARM, x86 | No |


**Then we will choice U-Boot boot-loader**

- **U-BOOT : **[﻿github.com/u-boot/u-boot](https://github.com/u-boot/u-boot) 
- **Red-Boot [Task]**: recipe for **YOCTO.**
---

Init-process:

1. Choose:
    1. System-D ---> How to deal with this ?
    2. System-V ---> How to deal with this ?


---

### **C-Library**
| Library | Configurable | YOCTO Support |
| ----- | ----- | ----- |
| GLIBC | YES | YES |
| UClibc | No | YES |


---

### **How to understand any software **Dynamically** ?**
Equation = `﻿Init + operate (states) + terminate.` 



---

### Linux Kernel Start-up
[﻿2. Linux Kernel Startup](https://app.eraser.io/workspace/4TjVUtUBV25tUZAuaMsv) 



📝 [**Presentation in 15 mins**] U-Boot supports `﻿init + operate + die (when gives control to kernel)` .


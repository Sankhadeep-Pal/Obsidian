## Problem:

![[WhatsApp Image 2025-07-02 at 4.13.57 PM.jpeg]]

## Solution:

![[ChatGPT Image Jul 2, 2025, 05_57_57 PM.png]]

- **Add those two phrases** at:
 
```
GRUB_CMDLINE_LINUX="rd.luks.uuid=luks-5e8292c6-c261-4621-9b33-06706314b56b rhgb quiet"
```

- `pcie_aspm=off` stops PCIe power-save (The main cause of the problem).
- `pci=noaer` suppresses the error (optional).


- **Update the grub** using:

```bash
sudo grub2-mkconfig -o /boot/grub2/grub.cfg
```


---

[![magicstick-logo](magicstick-logo.png)](https://github.com/samartzidis/magicstick.io)
###### Apple Keyboard USB Adapter for PCs

# About

MagicStick.io is a USB stick adapter to connect any Apple (Magic 1, Magic 2 or the older Apple Wireless) keyboard to a PC, providing the correct keymap translation for PCs. That is, you get a working Delete, Ctrl, Page Up/Down, Print Screen, Multimedia keys etc. You also get dual keyboard connection modes, wired and Bluetooth. All modern versions of Windows and Linux are supported.

Additionally, any device that accepts conventional USB keyboards should work with it, such as game consoles or smart TVs.
  
<table>
<body>
  <tr>
    <td>
    <a href="docs/6.png"><img src="docs/6_tn.png" alt=""></a>
    </br>
    Overview.
    </td>
    <td>
    <a href="docs/8.png"><img src="docs/8_tn.png" alt=""></a>
    </br>
    With a male PC</br>USB adaptor.
    </td>
    <td>
    <a href="docs/10.png"><img src="docs/10_tn.png" alt=""></a>
    </br>
    On wired connection.
    </td>
  </tr>
  <tr>
    <td>
    <a href="docs/11.png"><img src="docs/11_tn.png" alt=""></a>
    </br>
    On wired</br>connection.
    </td>
    <td>
    <a href="docs/12.png"><img src="docs/12_tn.png" alt=""></a>
    </br>
    On Bluetooth</br>connection.
    </td>    
    <td>
    <a href="docs/9.png"><img src="docs/9_tn.png" alt=""></a>
    </br>
    For the curious.
    </td>
  </tr>
  </body>
</table>

MagicStick.io started as a personal hobby project, inspired by my need to connect the excellent quality but "eccentric" Apple keyboard peripherals to my PC, without having to develop any special kernel-mode drivers and after realizing the ideal potential (e.g. speedy cores, powerful PIO subsystem, Bluetooth chip) of the Raspberry Pi Pico/RP2040 board. The plastic case was designed by my 6 y.o. daughter with a little bit of help from me :)

You can order a hand-made MagicStick.io device from [![magicstick-logo](docs/etsy.png)](https://www.etsy.com/your/shops/MagicStickIO) 

The rest of the software stuff, such as documentation, utilities and firmware updates are here.

## User Manual

The user manual is [here](docs/README.md).

## Currently Supported Apple Keyboard Models

| Model | Status |
| -------- | ------- |
| A1314 | Old keyboard. Supported but no UI battery level indicator in MagicstickUI. |
| A1644 | Fully supported. |
| A2450 | Fully supported. |
| A2449 | Supported - but no fingerprint sensor (yet!). |

## Features

- MagicStick.io is powered by a Raspberry Pi Pico board with a **133MHz dual-core Arm Cortex M0+** processor. All processing logic is implemented in **optimized C/C++ and assembly** code, utilizing both processor cores. The dual USB stack is managed by the first core and the Bluetooth stack is managed by the second core, unless Bluetooth is disabled, and the secondary PIO-backed USB stack is managed by the second core.
- MagicStick.io can function **both wired and wirelessly**. You can connect your Apple keyboard either via a standard USB to Lightning cable or wirelessly via Bluetooth. You can freely switch between wired or wireless connection modes at any time.
- Wired and Bluetooth operation modes provide **surprisingly fast response times**. Tests performed with online measurement tools could not detect any extra delays over the default 16ms rebounce delay of the A1644 keyboard).

  ![](docs/20231001222021.png)
  
_The above measurement on [clickspeedtester.com](https://www.clickspeedtester.com) using an A1644 keyboard, averaged the same between (all) MagicStick-wired, MagicStick-Bluetooth, and direct PC USB (that is without MagicStick and with no extra Windows drivers installed)_.
- MagicStick.io is a microcontroller-based device. It **works immediately** as soon as it is powered on. This allows you to use the keyboard as early as at the PC boot process, e.g. for accessing the BIOS/UEFI menus. Also since there is no Operating System driver required, the keyboard just works correctly in BIOS/UEFI mode.
- MagicStick.io is **programmable** so that you can reposition almost all keys as you like.
- MagicStick.io supports an OS **battery level indicator** in both wired and wireless connection modes in both **Windows** and **Linux**. Ubuntu Linux natively supports a battery-level indicator whereas for Windows you can use the MagicStickUI utility.
- MagicStick.io is built with **security** in mind. It is locked down to standard keyboard HID API on the side that connects to the PC. The Bluetooth connection uses a licensed [BlueKitchen](https://bluekitchen-gmbh.com/) Bluetooth stack with Level 2 security enabled (wireless encryption). Additionally, Bluetooth can be disabled if needed.
- In contrast to other similar solutions (e.g. MagicUtilities), MagicStick.io has **no subscription fees** or any connected device restrictions. You own the device, and you can connect it to **as many keyboards or computers** as you like.
- **PC sleep/wake-up** is supported and works **in both wired and Bluetooth** connection modes.
- **Firmware updates**. Any future improvements, such as support for new keyboard models are easy to install and provided for free.

(1) Tests were carried out using a reference Apple Magic Keyboard 2 keyboard using an online utility. Other third-party measurements: https://www.notebookcheck.net/Are-gaming-keyboards-really-faster-than-conventional-keyboards.258470.0.html

## Compliance and Safety

Technically, MagicStick.io just is a programmed Raspberry Pi Zero microcontroller. Please refer to this official link for further details on the compliance and safety of the Raspberry Pi Pico: https://pip.raspberrypi.com/categories/688

## Disclaimer

MagicStick.io was professionally developed with love and attention to detail, following software engineering best practices. There is no 100% guarantee however that it will work for your particular setup neither I accept responsibility for anything going wrong to your equipment or to you directly or indirectly through its use. By accepting to use the device you also accept full responsibility for all of the above. The MagicStick.io hand-made devices are returnable as per the Etsy shop policy.


 








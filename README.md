<p align="center"><img src="https://github.com/K3V1991/Device-not-connecting-to-PC-in-Fastboot-Mode/blob/main/USB.png" width="200"></a>
<h1 align="center"><b>Device not connecting to PC in Fastboot Mode</b></h1>
<h4 align="center">Simple Guide so that your Windows PC can easily detect Android Devices through the Fastboot Command</h4>
<br />

<p align="center">
<a href="https://liberapay.com/K3V1991" alt="LiberaPay"><img src="https://img.shields.io/badge/Liberapay-F6C915?style=for-the-badge&logo=liberapay&logoColor=black" /></a>
<a href="https://ko-fi.com/k3v1991" alt="Ko-fi"><img src="https://img.shields.io/badge/Ko--fi-F16061?style=for-the-badge&logo=ko-fi&logoColor=white" /></a>
<a href="https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=HW8B98TVDLKWA" alt="PayPal"><img src="https://img.shields.io/badge/PayPal-00457C?style=for-the-badge&logo=paypal&logoColor=white" /></a>
<a href="https://github.com/K3V1991/Donate-Crypto/blob/main/README.md" alt="Crypto"><img src="https://img.shields.io/badge/Bitcoin-000?style=for-the-badge&logo=bitcoin&logoColor=white" /></a>
</p>
<hr />
<br />

## Unable to connect to ADB:
<details>
  <summary>Click to expand</summary>
  
1. AMD Bug - [XDA Thread](https://forum.xda-developers.com/t/fix-fastboot-issues-on-ryzen-based-pcs.4186321/)
2. Switch Device from ```Charging``` to ```File Transfer``` Mode
3. Install the latest Device Driver or Universal USB Driver
4. Try another USB Cable
5. Use another USB Port (USB 3.0 Port to USB 2.0)
6. Try to execute Fastboot Command without connecting your Device, and once it says ```waiting for device``` plug in your USB Cable
7. Windows: Click ```Change advanced power setting``` on your chosen Plan and expand ```USB Settings```. Under ```USB Settings``` Section, expand ```USB selective suspend setting``` and change it to ```Disabled``` for On Battery and Plugged In
8. Try another PC
</details>
<br />

## How-To:
1. Download the latest Fastboot Driver - [Google USB Driver](https://developer.android.com/studio/run/win-usb)
2. Extract the ZIP File
3. Connect your Device to the PC. If ADB is working for you, you can simply run ```adb reboot bootloader``` to instantly move to Fastboot Mode
4. Press the ```Windows + X``` Keyboard Shortcut on Windows 10 and open ```Device Manager```
5. Expand the ```Portable``` or ```Other devices``` Menu and you will find your Android Device. It will display a yellow Sign next to it which means Fastboot is not working on your Computer. Right-click on it and click on ```Update driver```
6. A new Window will open up. Click on ```Browser my computer for drivers```
7. On the next Page, click on ```Browse...``` and select the Fastboot Driver Folder that you extracted above. You just need to select the Folder and not any specific File. Device Manager will automatically find the ```android_winusb.inf``` File
8. Once you have selected the Folder, click on ```Next```
9. Now, it will install the Fastboot Drivers on your PC
10. Find your Android Device move to the Top Menu on Device Manager and the name will change to ```Android Bootloader Interface```
11. Open a Command Prompt Window and run the ```fastboot devices``` Command. This Time, it will detect your Device 

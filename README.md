# AIR_GAPPED Implementation  

This is an implementation of an air-gapped system to securely store all my backups and passwords.  

## Used Devices  
- **Android 9 Tablet**  

## Software Used  
- **Android SDK**  
- **F-Droid**  

## Objective  
To create a fully air-gapped system for storing passwords completely offline and encrypted.  

## Steps  
1. Download and install **Android SDK** on your PC.  
2. Connect the device and enable **USB Debugging** on it.  
3. Open **Command Prompt (cmd)** and navigate to the SDK folder.  
4. Type `"adb devices"` to check if your device is connected.  
5. Type `"adb shell pm list packages | findstr #device_maker"` (replace `#device_maker` with your device brand, e.g., `adb shell pm list packages | findstr samsung`).  
6. You will now see all the preinstalled services. To ensure the device is air-gapped and secure, remove any vulnerabilities:  
   - **Option 1**: Disable the service.  `adb shell pm disable-user --user 0 #service_name`
   - **Option 2**: Uninstall the service (**cannot be reversed**).  `adb shell pm uninstall --user 0 #service_name`
7. Before disabling or uninstalling Wi-Fi-related services, install a password manager and a file manager. I chose to stay open-source and downloaded **KeepassDX** from **F-Droid**.  
8. Download any other safe and open-source applications you may need.  
9. Disable **Wi-Fi** and any other network-related services.  
10. Add extra security measures:  
    - **App password protection**  
    - **Secure lock screen password**  
    - **Reset device on multiple failed login attempts**  

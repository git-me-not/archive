1. enable 32-bit architecture
   ```dpkg --add-architecture i386``` 

3. install steam installer from debian repository
   ```apt install --no-install-recommends steam-installer```
   * ```apt install --no-install-recommends xdg-desktop-portal xdg-desktop-portal-gtk``` for file picker

5. install necessary package/libraries for vulkan (Intel)
   ```apt install mesa-vulkan-drivers libglx-mesa0:i386 mesa-vulkan-drivers:i386 libgl1-mesa-dri:i386 libva-drm2``` 

4steam. add your user to render group
 ```usermod -aG render $USER``` 

# Cymatune LT

Cymatune LT is an app, focused on:
- Fake tower (IMSI catcher/Stingray) recognition
- Tower location and triangulation

## Features

- **Fake Tower Detection**: Identifies and alerts about potential IMSI catchers or Stingrays in your vicinity.
- **Tower Location & Triangulation**: Provides accurate location and triangulation of cellular towers.
- **Minimal Footprint**: Optimized for low resource consumption and fast deployment.

## Running

To run the Cymatune LT application, follow these steps:

1.  **Prerequisites**:
    *   An Android device or emulator with Android Debug Bridge (ADB) configured.

2.  **Install on Device/Emulator**:
    Install via the APK found on play store on a connected Android device or emulator

## Granting ADB Permissions

Cymatune LT requires specific permissions to function correctly, which are granted via Android Debug Bridge (ADB).

### On the Android Device

1.  **Enable Developer Options**:
    *   Go to `Settings` > `About phone` (or `About tablet`).
    *   Tap `Build number` seven times rapidly until you see a message "You are now a developer!"
2.  **Enable USB Debugging**:
    *   Go to `Settings` > `System` > `Developer options`.
    *   Find and enable `USB debugging`.
3.  **Revoke USB debugging authorizations (Optional but Recommended)**:
    *   In `Developer options`, find `Revoke USB debugging authorizations` and tap it. This ensures a fresh authorization prompt.

### From the Desktop (PC)

1.  **Install ADB**:
    *   Download the Android SDK Platform-Tools from the official Android Developers website.
    *   Extract the downloaded ZIP file to a convenient location (e.g., `C:\platform-tools`).
    *   Add the `platform-tools` directory to your system's PATH environment variable.
2.  **Connect Device**:
    *   Connect your Android device to your PC using a USB cable.
3.  **Verify Connection**:
    *   Open Command Prompt or PowerShell.
    *   Type `adb devices` and press Enter. You should see your device listed with "unauthorized" status.
4.  **Authorize Device**:
    *   On your Android device, a prompt will appear asking to "Allow USB debugging?". Check "Always allow from this computer" and tap "OK".
5.  **Verify Authorization**:
    *   Run `adb devices` again on your PC. Your device should now be listed with "device" status.

### From the Desktop (Mac)

1.  **Install ADB**:
    *   Download the Android SDK Platform-Tools from the official Android Developers website.
    *   Extract the downloaded ZIP file to a convenient location (e.g., `~/platform-tools`).
    *   Open Terminal and add the `platform-tools` directory to your shell's PATH. For example, if you use zsh:
        ```bash
        echo 'export PATH=$PATH:~/platform-tools' >> ~/.zshrc
        source ~/.zshrc
        ```
        (Replace `~/.zshrc` with `~/.bash_profile` or `~/.bashrc` if you use Bash.)
2.  **Connect Device**:
    *   Connect your Android device to your Mac using a USB cable.
3.  **Verify Connection**:
    *   Open Terminal.
    *   Type `adb devices` and press Enter. You should see your device listed with "unauthorized" status.
4.  **Authorize Device**:
    *   On your Android device, a prompt will appear asking to "Allow USB debugging?". Check "Always allow from this computer" and tap "OK".
5.  **Verify Authorization**:
    *   Run `adb devices` again on your Mac. Your device should now be listed with "device" status.

## Disclaimer and Legal Information

**THIS SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.**

**Cymatune LT is currently in a testing phase. While efforts have been made to ensure accuracy, false positives may be possible. Users are advised to exercise caution and verify any alerts independently.**

**Copyright 2025 SandTuskers. All rights reserved.**

This is a closed-source application. However, certain components and concepts within Cymatune LT are inspired by or utilize elements from open-source projects. We extend our gratitude and acknowledge the following:

*   **LogcatReader**: The foundational concept and initial structure for reading logcat data in Cymatune LT were inspired by the project found at [https://github.com/darshanparajuli/LogcatReader](https://github.com/darshanparajuli/LogcatReader).
*   **AIMSCID (Android IMSI Catcher Detector)**: Portions of the fake tower detection logic and methodologies are influenced by the work found at [https://github.com/CellularPrivacy/Android-IMSI-Catcher-Detector/wiki](https://github.com/CellularPrivacy/Android-IMSI-Catcher-Detector/wiki).
*   **Snoopsnitch**: Concepts related to cellular network security analysis and detection mechanisms are informed by the principles demonstrated in Snoopsnitch, which can be explored at [https://github.com/srlabs/snoopsnitch](https://github.com/srlabs/snoopsnitch).
*   **OpenStreetMap**: Mapping functionalities within Cymatune LT utilize data from OpenStreetMap. Attribution is given to "© OpenStreetMap contributors". More information can be found at [https://www.openstreetmap.org/copyright](https://www.openstreetmap.org/copyright).

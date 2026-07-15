# Sanchez SimRacing Brake Pedal: User Guide

## What's in the Box

- Brake pedal controller unit
- USB cable

---

## Installation

The controller is designed to replace the potentiometer in your existing brake pedal.

### Signal Cables

The device has two cables:

| Cable color | Connect to |
|-------------|-----------|
| **Black** | Pedal harness ground wire |
| **White** | Pedal harness signal wire |

Match the cables to the ground and signal pins your original potentiometer was using. Leave the pedal harness **red (power) wire** connected to the original potentiometer; the controller does not use it.

### Power (USB)

The device is powered through its **USB** port. Connect it to:

- **Your PC**: required if you want to use the SimHub companion plugin (see [SimHub Plugin](#simhub-plugin))
- **Any 5 V power source**: such as a phone charger, if you only need the analog output

> **If the device keeps restarting on its own**, it is not receiving enough power. Try a different USB port on your PC (rear motherboard ports are usually more reliable than front-panel or hub ports) and avoid USB extension cables. This issue does not typically occur with phone chargers or other dedicated power adapters.

---

## Getting Started

### 1. Power On

Connect your pedal to the rig as normal. The controller powers up automatically.

### 2. First-Time Wi-Fi Setup

The pedal creates its own Wi-Fi network for configuration. A new password is generated on first boot, so you need to retrieve it once:

1. Hold the **button** for **3 seconds** to enter recovery mode. You will know you have held long enough when the light starts blinking very fast; release the button at that point (holding longer will trigger a factory reset).
2. On your phone or PC, scan for Wi-Fi networks. A network starting with **SS Brake Pedal** will appear; connect to it. No password is required in recovery mode.
3. The configuration page opens automatically. Your new Wi-Fi password is displayed on screen. **Save it somewhere safe.**

> **Tip:** On most phones and laptops, a "Sign in to network" or "Configuration page" popup will appear automatically after connecting. If not, open a browser and go to **http://192.168.4.1**.

From now on, press the **button** once to activate Wi-Fi, and use the saved password to connect.

### 3. Calibrate (optional)

The pedal is ready to use out of the box: zero calibration happens automatically on every boot, and the max range defaults to 100 % (full sensor capacity). If you want to adjust these to match your setup, see the [Calibration](#calibration) section.

---

## Status Light

| Light Pattern | Meaning |
|---------------|---------|
| Single pulse every 3 s | Normal operation |
| Double-flash, pause (repeating) | Wi-Fi config mode is active |
| Triple-flash, pause (repeating) | Recovery mode is active (no password) |
| Rapid continuous blink | Problem detected. Check all connections |
| Very rapid continuous blink | Factory reset countdown in progress |

---

## Button

| Press | Action |
|-------|--------|
| Short press | Turn Wi-Fi config mode on or off |
| Hold 3 seconds | Start **recovery mode** (no password required) |
| Hold 10 seconds | **Factory reset**: erases all settings |

---

## Wi-Fi Config Mode

The Wi-Fi hotspot turns off automatically after **5 minutes** with no activity. You can change this behaviour in [Settings](#settings).

To reconnect at any time, press the button again.

---

## Calibration

Open the web interface and scroll to the **Tuning** section (zero calibration and max range now live there, alongside the response curve and dead-zone).

### Set Zero Point

By default, the pedal automatically re-zeroes itself every time it powers on; just make sure the pedal is fully released during the first second or two after switching on your rig.

If you prefer a fixed zero that never changes on reboot, you can disable this in [Settings](#settings) (**Calibrate on startup**). You can then set the zero point manually at any time:

1. Completely release the brake pedal, with no pressure at all.
2. Tap **Zero Point**.

### Set Max Range

By default the pedal uses the full sensor range (100 %). If your setup or driving style calls for a lighter maximum, you can reduce it:

Drag the **Max Range** slider to the desired value (5–100 %) and release. The value saves automatically. A lower percentage means full braking output is reached with less physical force.

> **Re-calibrate whenever:** you mount the pedal in a new position, or notice the zero point has drifted after warming up.

---

## Profiles

Four profiles let you quickly switch between different feel presets, for example one for road racing and another for endurance or wet conditions.

Each profile stores its own max range, response curve, and dead-zone settings.

### Switching Profiles

Tap any profile button. The active profile is highlighted in red. Settings load immediately.

### Saving a Profile

Tuning changes take effect immediately, but they are not stored in any profile until you explicitly save. If you switch to a different profile and back, unsaved changes will be overwritten by whatever was last saved in that slot.

To save the current settings into the active profile:

1. Tune the response curve, dead-zone, and max range to your liking.
2. Tap **Rename** if you want to give it a name (up to 15 characters).
3. Tap **Save**.

---

## Tuning

The **Tuning** section holds everything that shapes the pedal feel (the response curve, dead-zone, max range, and zero calibration) in one place.

### Response Curve

Controls how pedal force translates into braking output. The curve has **six points** you can drag, at 0, 20, 40, 60, 80 and 100 % of pedal input. Each point sets the braking output (0–100 %) at that input: drag it up for more output there, down for less. A point can't cross its neighbours, so the response always stays smooth and never reverses. A small white dot shows where your current pedal position sits on the curve.

**Presets** give you a one-tap starting point that you can then fine-tune by dragging:

| Preset | Feel |
|--------|------|
| **Linear** | Output matches input directly (1:1) |
| **S-Curve** | Softer at both ends, firmer through the middle |
| **Expo** | Extra sensitivity early in travel, for fine control when feathering |
| **Inverse** | Extra resolution near full press, good for a firm threshold-brake feel |

### Dead-zone

Percentage of pedal travel at the start that is ignored. Useful to prevent ghost braking from pedal flex or vibration.

- **0%**: no dead-zone; any movement registers
- **2–5%**: recommended starting point for most setups
- **Up to 20%**: for very sensitive or noisy setups

---

## Settings

| Setting | What it does |
|---------|--------------|
| **Stop on disconnect** | Turns off Wi-Fi as soon as you disconnect from the config page |
| **Keep Wi-Fi open** | Disables all automatic shutdown; the hotspot stays on until you turn it off manually |
| **Calibrate on startup** | Automatically re-zeroes the pedal every time it powers on |

> If **Keep Wi-Fi open** is enabled, **Stop on disconnect** is automatically overridden.

---

## Live Pressure Graph

The **Live Pressure** section shows a scrolling 6-second graph of your brake input:

- **Red line**: the actual output signal sent to your sim (after the response curve)
- **Faint line**: your raw pedal input for reference

---

## Hardware Status

The **Hardware** section shows a green **✓ OK** when everything is working correctly. If an error code is shown in red, there is an internal hardware fault:

| Code | Meaning |
|------|---------|
| **E01** | Load cell sensor problem |
| **E02** | Analog output problem |

If either code appears, check all cable connections and power-cycle the pedal. If the error persists, please contact **Sanchez SimRacing** for support.

---

## Firmware Update

The web interface includes a **Firmware** section at the bottom of the page. It shows the current firmware version and lets you install a new one.

The pedal's Wi-Fi does not provide internet access. Your phone cannot download anything while it is connected to the pedal, so downloading the file and installing it are two separate steps.

**Step 1: download the file.** While you still have internet, on any device, go to:

**sanchezsimracing.com.ar/firmware**

Download the **.bin** file from the latest release. The **Firmware** section of the web interface shows this same address, and you can tap it to copy it.

**Step 2: install it.**

1. Connect to the pedal's Wi-Fi and open the web interface.
2. Tap **Select .bin file** and choose the file you downloaded.
3. Tap **Update Firmware** and confirm when prompted.
4. A progress bar shows the upload status. Once complete, the device reboots automatically with the new firmware.

> **Note:** Only firmware files signed by Sanchez SimRacing will be accepted. If the file is invalid or unrecognized, the update will be rejected and no changes will be made.

---

## SimHub Plugin

A companion plugin for [SimHub](https://www.simhubdash.com/) lets you configure and monitor the pedal directly from your PC, with no Wi-Fi required. The USB cable must be connected to the PC.

### Installing the Plugin

1. Download **SSBrakePedal.dll** from the link provided by Sanchez SimRacing.
2. Copy the file into the SimHub installation folder (typically `C:\Program Files (x86)\SimHub\`).
3. Restart SimHub.

The plugin appears under **Additional Plugins → SS Brake Pedal** in the left menu.

### Connecting

The plugin auto-detects the pedal on any COM port when SimHub starts. If it doesn't connect automatically (for example, the pedal was plugged in after SimHub started), open the plugin panel and click **Connect**.

> The device takes up to ~5 seconds to finish booting when first powered on. The plugin waits long enough to handle this.

### What You Can Do from SimHub

| Feature | Description |
|---------|-------------|
| **Live Brake Position** | Real-time bars showing both the curved output (what the game sees) and the linear raw input |
| **Response curve / Deadzone / Max Range** | The same tuning controls as the web interface. Drag a point or pick a preset, and changes apply immediately |
| **Set Zero** | Re-calibrate the zero point without opening the web interface |
| **Profiles** | Load, rename, and save any of the four profiles |

> All settings changed through SimHub are saved on the device and persist after reboot; they are the same settings you see in the Wi-Fi web interface.

---

## Language

Tap the language selector (EN / ES) in the top-right corner of the web page. The preference is saved on the device.

---

## Forgot or Change the Wi-Fi Password

Hold the button for **3 seconds** to enter recovery mode. This generates a new password and opens the Wi-Fi network without requiring the old one. Connect to the **SS Brake Pedal** network and the web interface will display your new password; save it somewhere safe.

After reboot, the new password is required.

---

## Factory Reset

A factory reset erases all profiles, calibration data, and settings, and generates a new Wi-Fi password.

**To factory reset:**
- Hold the button for **10 seconds** (the light will blink very fast as a countdown warning)

After the reset the device reboots and starts fresh. You will need to calibrate and configure it again.

---

## Reboot

Tap **Reboot Device** at the bottom of the web interface (tap twice to confirm). The device restarts in a few seconds.

---

## Support

For any questions or issues, reach us at:

**support@sanchezsimracing.com.ar**

# Vaxp Updater

![vaxp_updater main screen](screenshot/Screenshot%20from%202025-11-03%2014-05-08.png)

## Overview

`vaxp_updater` is the official application and update manager for the VAXP-OS system. It is designed to be lightweight, fast, and fully integrated with the VAXPDE desktop environment, providing a seamless user experience for managing all VAXP applications.

The application is built using Flutter and follows VAXPDE's visual identity (glass-like dark theme).

---

## Key Features

* **System Discovery:** Displays a list of all available VAXP system applications.
* **Status Management:** Shows the status of each application (Installed, Not Installed, or Update Available).
* **One-Click Installation:** Enables direct installation of new applications (like `VaxManager`) directly from the interface.
* **Changelog Display:** Shows a confirmation popup including the changelog before starting installation.
* **Application Updates:** Provides "Check for Update" buttons to check and update installed applications to the latest version.
* **Native System Integration:**
    * Uses `polkit` (PolicyKit) to securely request authentication (user password) before making system changes.
    * Uses `apt` in the background to properly handle installation and updating of `.deb` packages.
* **Immediate Feedback:** Displays clear notifications (Snackbar) upon operation success or failure.

![Application details and changelog](screenshot/Screenshot%20from%202025-11-03%2014-05-17.png)
![Update process](screenshot/Screenshot%20from%202025-11-03%2014-05-26.png)
![Installation complete](screenshot/Screenshot%20from%202025-11-03%2014-05-36.png)

---

## Project Goal

The primary goal of `vaxp_updater` is to provide a centralized and trusted "store" or "control center" to ensure VAXP-OS users can easily obtain the latest applications, security updates, and fixes for the VAXP system.

---

## Dependencies

To function properly, `vaxp_updater` requires the following components in the system:
* `flutter` (Linux Desktop)
* `apt` (for package management)
* `polkit` (for authentication management)

---

## Installation

`vaxp_updater` is an essential part of the VAXP-OS system and comes pre-installed. It can also be manually installed via the official `.deb` package.

```bash
sudo apt install ./vaxp_updater_v0.1.0.deb
```
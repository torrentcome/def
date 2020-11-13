# Hdcp
## HDCP = High-bandwidth Digital Content Protection

It'ss a form of digital copy protection developed by Intel Corporation[1] to prevent copying of digital audio and video content as it travels across connections. Types of connections include DisplayPort (DP), Digital Visual Interface (DVI), and High-Definition Multimedia Interface (HDMI), as well as less popular or now deprecated protocols like Gigabit Video Interface (GVIF) and Unified Display Interface (UDI).

### HDCP uses three systems

- Authentication prevents non-licensed devices from receiving content.
- Encryption of the data sent over DisplayPort, DVI, HDMI, GVIF, or UDI interfaces prevents eavesdropping of information and man-in-the-middle attacks.
- Key revocation prevents devices that have been compromised and cloned from receiving data.

### On Android
- try to check the Display flags: http://developer.android.com/reference/android/view/Display.html#getFlags()

- FLAG_SECURE or FLAG_SUPPORTS_PROTECTED_BUFFERS (http://developer.android.com/reference/android/view/Display.html#FLAG_SECURE and http://developer.android.com/reference/android/view/Display.html#FLAG_SUPPORTS_PROTECTED_BUFFERS)

# Lab 01 – document initial Dell Inspiron 15 5000-series 2-in-1 inspection and diagnostics

## Objective
Discover actual condition of used/unknown history Dell Inspiron 15 5000-series 2-in-1

## Scenario
Laptop purchased from Goodwill auction used/unknown history.

## Environment
- Device / VM: Dell Inspiron 15 5000-series 2-in-1 
- Operating system: Windows (need to verify edition)
- Hardware: Intel Core i5-8250U, 8 GB DDR4-2400, one 8 GB DIMM installed, 256 GB SATA storage, 15.6" 1920×1080 display, 
- Network: Qualcomm Wi-Fi
- Safety/isolation notes: 

## Tools Used
- BIOS / DELL ePSA diagnostics
- Chat GPT
- Mini Phillips screw driver
- Anti Static wrist wrap

## Initial Symptoms
- Front LED shows 4 amber flashes → 1 white flash → pause → repeat when the charger is plugged in.
- Bios showed battery fault 
- Bubbles noticed in the 4 corners of the screen
- Brightness wouldn't go up or down despite the graphic meter moving

## Pre-Work Data / Privacy Check
- [x] Important data identified.
- [x] Backup need evaluated before invasive changes.
- [x] Evidence/screenshots are sanitized for public GitHub use.

## Diagnostic Process
1. Reviewed BIOS system information and battery status. BIOS initially reported that the battery was not installed.
2. Ran Dell ePSA pre-boot diagnostics. Initial testing also indicated that the battery was not detected.
3. Removed the bottom cover and visually inspected the battery, battery connector, charging jack area, and accessible motherboard connections. No obvious physical damage, swelling, or bent connector pins were observed.
4. Disconnected the internal battery and attempted AC-only operation using the original Dell-style AC adapter.
5. With the battery disconnected, the repeating 4-amber / 1-white front LED code was no longer present, but the system reported that the AC adapter wattage/type could not be determined.
6. Tested the laptop with a replacement 65 W Dell AC adapter. BIOS correctly identified the replacement adapter as 65 W.
7. Reconnected the internal battery and retested the system using the replacement AC adapter.
8. BIOS then detected the battery, reported battery health as Excellent, and showed the battery charging normally.
9. Charged the battery to 100% and performed an initial unplugged runtime test. Battery discharge appeared normal and Windows estimated several hours of remaining runtime.
10. Re-ran Dell ePSA diagnostics with the laptop fully reassembled to verify operation after troubleshooting.
11. Performed preliminary touchscreen testing using Microsoft Paint. Touch input registered across the main display area despite visible cosmetic bubbling/delamination near portions of the display.
12. Observed that Windows brightness controls did not change panel brightness. Device Manager showed Microsoft Basic Display Adapter and several unidentified devices, indicating that the existing Windows installation is missing required Dell/Intel drivers. Brightness control operated correctly in BIOS, supporting a software/driver cause rather than a backlight hardware failure.

## Evidence
<img width="1152" height="1536" alt="image-1787606755425" src="https://github.com/user-attachments/assets/68da93e3-d93c-4e6b-a0db-5e7844c3e0ac" />
*Dell BIOS system-information screen used to verify installed processor, memory, storage, and hardware configuration.*
<img width="1152" height="1536" alt="image-1787606800457" src="https://github.com/user-attachments/assets/cfa4da9e-9830-4202-81b0-d20b9978137c" />
*BIOS battery information showing that the internal battery was initially reported as not installed/detected.*
<img width="1152" height="1536" alt="image-1787606771786" src="https://github.com/user-attachments/assets/2a765980-43f0-4600-b858-e25f91a0f634" />
*Dell ePSA pre-boot diagnostic testing performed to evaluate the laptop independently of the installed Windows environment.*
<img width="1152" height="1536" alt="image-1787616860042" src="https://github.com/user-attachments/assets/3cb4f1dc-e4dc-4eb3-9cb9-a3c192263c17" />
*ePSA diagnostic information confirming the initial battery-detection issue observed in BIOS.*
<img width="1152" height="1536" alt="image-1787617200271" src="https://github.com/user-attachments/assets/362b81c6-643d-42fb-95ff-243192de7760" />
*Bottom cover removed for internal hardware inspection and battery troubleshooting.*
<img width="1152" height="1536" alt="image-1787617253442" src="https://github.com/user-attachments/assets/238eb82d-7ac8-4050-b5ed-e02d3f8c3f65" />
*Internal overview showing the battery, motherboard, cooling system, memory, and storage components.*
<img width="1152" height="1536" alt="image-1787617323418" src="https://github.com/user-attachments/assets/2c366c4f-da6e-46f5-a7ef-5f0b77626687" />
*Visual inspection of the internal battery showed no obvious swelling or physical deformation.*
<img width="1152" height="1536" alt="image-1787617358523" src="https://github.com/user-attachments/assets/04bdd29b-6370-4526-83e4-27ac0219ba42" />
*Closer inspection of the battery and surrounding chassis for signs of swelling, leakage, or physical damage.*
<img width="1152" height="1536" alt="image-1787617343940" src="https://github.com/user-attachments/assets/d6c3e443-11f3-4ab8-b214-e16463ac1999" />
*Battery connector and motherboard connection inspected for loose seating, bent contacts, or visible damage.*
<img width="1152" height="1536" alt="image-1787617441844" src="https://github.com/user-attachments/assets/3b81eaff-6044-445a-889f-5c5db261b4fc" />
*Internal power/charging components visually inspected while troubleshooting the battery and adapter fault indication.*
<img width="1152" height="1536" alt="image-1787617427736" src="https://github.com/user-attachments/assets/7c6f31c3-ce2f-4277-b5f5-766f141c14a2" />
*Installed memory and internal components inspected as part of the hardware-condition assessment.*
<img width="1152" height="1536" alt="image-1787617454000" src="https://github.com/user-attachments/assets/dadb988a-f48f-408b-9d82-b0d33f9578c3" />
*Storage and other accessible internal hardware inspected for obvious damage or loose connections.*
<img width="1152" height="1536" alt="image-1787617464992" src="https://github.com/user-attachments/assets/b448d055-b82a-4152-9213-2325d56c5e75" />
*Additional internal inspection performed before reassembly and follow-up electrical testing.*
<img width="1152" height="1536" alt="image-1787617464992 (1)" src="https://github.com/user-attachments/assets/1e784dd8-f2ab-459f-bb6f-7420e8a624ef" />
*System configuration and diagnostic information recorded to establish a baseline before repair or operating-system changes.*
<img width="1152" height="1536" alt="image-1787617295641" src="https://github.com/user-attachments/assets/1436ec65-436b-4574-bbbd-5e4349029457" />
*Final evidence from the initial inspection documenting the laptop’s hardware condition prior to continued troubleshooting.*
<img width="1536" height="1152" alt="image-1787617580740" src="https://github.com/user-attachments/assets/500423ed-9a7b-4ccb-a451-27e7ea15eb6d" />
<img width="1152" height="1536" alt="image-1787617564431" src="https://github.com/user-attachments/assets/b2eed70e-8bb1-4505-9e89-c5089d128d72" />
<img width="1152" height="1536" alt="image-1787617548708" src="https://github.com/user-attachments/assets/165ffefd-2e5b-48a7-b7ee-f5106da69168" />

## Findings
**Root cause / most likely cause:**  
The original AC adapter was defective or unable to properly communicate its identification/wattage information to the laptop. The laptop itself was able to correctly identify a known-good replacement 65 W Dell adapter.

The internal battery was initially suspected because BIOS and ePSA reported that it was not installed and the laptop displayed a repeating front LED fault indication. Subsequent testing showed that the battery itself was functional.

**Why the evidence supports it:**  
The original adapter powered the laptop but BIOS could not reliably identify the adapter type/wattage.
The front LED fault indication stopped when the battery was disconnected.
A replacement Dell 65 W adapter was immediately identified correctly by BIOS.
After reconnecting the existing battery while using the replacement adapter, BIOS detected the battery and reported its health as Excellent.
The battery successfully charged to 100% and operated the laptop on battery power.
No obvious physical damage was found at the battery connector, battery pack, or accessible charging components.
Brightness control works in BIOS but not in the current Windows installation. Device Manager shows Microsoft Basic Display Adapter and several missing platform drivers, indicating that the Windows brightness issue is software/driver related.
The display has visible cosmetic bubbling/delamination, but touchscreen testing in Paint showed functional touch response across the tested display area.

## Repair / Remediation
1. Replaced the suspect AC adapter with a known-good 65 W Dell-compatible adapter.
2. Reconnected and reseated the existing internal battery.
3. Reassembled the laptop and secured the bottom cover.
4. Verified correct AC adapter identification and battery charging in BIOS.
5. Deferred Windows driver remediation because the existing operating-system installation is considered untrusted and will be replaced with a clean Windows installation before the system is placed on a trusted network.

## Validation
- [x] Original charging/fault symptom retested.
- [x] Replacement AC adapter correctly identified in BIOS.
- [x] Existing battery detected and charging.
- [x] Battery charged to 100%.
- [x] Battery-only operation verified.
- [x] System restart/boot verified.
- [x] Bottom cover reinstalled and system retested fully assembled.
- [x] Touchscreen function tested across display area.
- [x] No obvious new hardware faults introduced.
- [x] Complete clean Windows installation.
- [x] Install current Dell/Intel device drivers.
- [x] Verify Windows brightness control after graphics driver installation.
- [x] Complete Windows Update.
- [x] Perform final Device Manager check for unknown devices or warnings.
- [x] Complete security/privacy validation before connecting to normal production/home network use.

## Security Check
- Updates: Clean installation of Windows 11 Home completed. Dell/Intel drivers installed and Windows Update completed.
- Endpoint protection: Microsoft Defender real-time protection enabled. Quick scan on October 1, 2026 found 0 threats. Security intelligence reported up to date on October 2, 2026.
- Firewall: Microsoft Defender Firewall enabled for Domain, Private, and Public network profiles.
- Secure Boot / TPM: Secure Boot enabled; TPM 2.0 ready to use. Windows Security reports Secure Boot certificate updates temporarily paused due to a known compatibility issue. Warning persists after the BIOS update and remains unresolved.
- Encryption: Device encryption enabled; Protection On confirmed after the BIOS update. Matching recovery-key backup verified in the Microsoft account.
- Accounts: Personal Microsoft account currently used for testing. Removal of personal accounts and stored credentials pending final resale preparation.

## Result
**Status:** Improved
The Dell Inspiron 15 5579 now recognizes the replacement 65W charger and charges the original battery. The previous adapter-identification warning and flashing amber indicator cleared. BIOS reports battery health as Excellent, so the original battery was retained.

A clean installation of Windows 11 Home is activated with a digital license. Dell/Intel drivers and Windows updates were completed, and brightness controls now work. BIOS was updated to version 1.19.0.

Display condition: Visible screen bubbles remain, although they are less noticeable at maximum brightness. This condition will be disclosed before sale.

Security limitation: The Secure Boot certificate-update warning remains after the BIOS update. Secure Boot is enabled, and TPM 2.0 is ready to use.

Current status: Repair and Windows installation work completed. Final app-protection verification, preservation of project records, personal-account cleanup, and the final resale reset remain pending.

## Lessons Learned
Verify charger recognition before replacing the battery. The original adapter powered the laptop, but BIOS reported it as Unknown. Testing a recognized 65W adapter restored charging and allowed the original battery to be retained.

Compare BIOS and Windows behavior when troubleshooting. Brightness adjustment worked in BIOS but failed in Windows. Dell/Intel driver updates restored Windows brightness controls.

Preserve recovery access during firmware updates. Match the recovery-key ID to the correct device before updating firmware, and confirm encryption protection is enabled afterward.

Verify the outcome of each change. The BIOS update completed successfully, but the Secure Boot certificate-update warning remained. A completed update should be followed by verification of the original symptom.

Document remaining limitations honestly. Screen bubbles remain despite restored brightness controls. Record unresolved issues, disclose them before sale, and mark unfinished resale preparation as pending.

## Skills Demonstrated
- Troubleshooting
- Documentation
- Customer-data awareness
- Validation / quality control
- Security-first repair methodology

# Lab 2 – Forensic USB Acquisition and Hash Verification

## 1. Overview

This practical laboratory exercise demonstrates the forensic acquisition and integrity verification of a USB flash drive using an approved forensic imaging methodology.

The exercise was performed using **Exterro FTK Imager 8.3.0.27** on a Windows forensic workstation. The USB device was identified, documented, acquired as a Raw/DD forensic image, cryptographically hashed, and subsequently verified.

The exercise demonstrates the following forensic principles:

* Identification and documentation of digital evidence.
* Controlled acquisition of a USB storage device.
* Creation of a forensic image without intentionally modifying the source evidence.
* Calculation of cryptographic hash values.
* Verification of forensic image integrity.
* Validation of the expected evidence file within the acquired image.
* Documentation of the acquisition process using screenshots and forensic notes.

---

## 2. Practical Scenario

A Kingston DataTraveler USB flash drive was submitted for examination as a controlled test evidence device.

The USB contained a student-created evidence folder and text file prepared specifically for this laboratory exercise.

The USB was treated as the source evidence. A forensic image was created using FTK Imager and stored separately on the computer's D: drive. The resulting image was then verified using cryptographic hashes and examined to confirm that the expected evidence file was present.

---

## 3. Objectives

The objectives of this practical exercise were to:

1. Identify the submitted USB storage device.
2. Document the relevant characteristics of the evidence.
3. Prepare the USB for controlled forensic acquisition.
4. Acquire a forensic image using FTK Imager.
5. Calculate cryptographic hash values.
6. Verify the integrity of the acquired forensic image.
7. Confirm the presence of the expected evidence file.
8. Document the acquisition and verification process.
9. Maintain appropriate forensic evidence documentation.

---

## 4. Evidence Information

| Evidence Attribute     | Details                              |
| ---------------------- | ------------------------------------ |
| Case/Lab ID            | SBT-DF202-Lab2                       |
| Evidence Number        | 001                                  |
| Evidence Type          | USB Flash Drive                      |
| Manufacturer           | Kingston                             |
| Device Model           | Kingston DataTraveler 3.0 USB Device |
| Serial Number          | Not reliably displayed by FTK Imager |
| Storage Capacity       | 59006 MB                             |
| File System            | FAT32                                |
| Source Device          | `\\.\PHYSICALDRIVE1`                 |
| Drive Interface        | USB                                  |
| Removable Drive        | Yes                                  |
| Examiner               | Kafayat Omolara Animashawun          |
| Student ID             | 2025/FWSD/11317                      |
| Host Computer          | OG                                   |
| Operating System       | Windows 11 Pro                       |
| Acquisition Tool       | Exterro FTK Imager 8.3.0.27          |
| Acquisition Method     | Physical device acquisition          |
| Image Format           | Raw/DD                               |
| Image Storage Location | `D:\ICDFA\CIP-B102-Lab4\`            |
| Acquisition Status     | Successful                           |

---

## 5. Evidence Preparation

A controlled evidence folder was created on the test USB:

```text
CIP-B102-Lab4-Evidence
```

The following evidence file was created inside the folder:

```text
kafayat_animashawun.txt
```

The file contained the following information:

```text
Full Name: Kafayat Omolara Animashawun
Registration Number: 2025/FWSD/11317
Date: 30 August 2026

Statement:
This USB was prepared by me for a controlled forensic acquisition laboratory exercise.
```

The USB was used as a personal/instructor-approved test device for this practical exercise.

### Screenshot Evidence

Screenshots showing the creation of the evidence folder, creation of the text file, and contents of the text file are included in the `screenshots` directory.

---

## 6. Tools and Resources Used

The following tools and resources were used:

* **Exterro FTK Imager 8.3.0.27** – forensic acquisition, examination and image verification.
* **Windows 11 Pro** – forensic acquisition workstation.
* **Windows PowerShell** – independent SHA-256 hash calculation.
* **Kingston DataTraveler 3.0 USB Device** – test evidence source.
* **GitHub** – storage of supporting documentation and screenshots.

---

## 7. Evidence Identification

Before acquisition, the USB device was carefully identified in FTK Imager.

The source was identified as:

```text
\\.\PHYSICALDRIVE1
```

FTK Imager identified the physical device as:

```text
Kingston DataTraveler 3.0 USB Device
```

The device reported a source data size of:

```text
59006 MB
```

The USB contained a FAT32 partition of approximately 59006 MB.

The correct USB device was confirmed before beginning the acquisition to reduce the risk of accidentally selecting another storage device.

### Screenshot Evidence

A screenshot documenting the identification and selection of the correct USB device is included in the `screenshots` directory.

---

## 8. Forensic Image Acquisition

The physical USB device was acquired using **Exterro FTK Imager 8.3.0.27**.

The acquisition method selected was **Raw/DD**.

The image was stored separately from the source USB on the computer's D: drive:

```text
D:\ICDFA\CIP-B102-Lab4\
```

The resulting forensic image was automatically divided into multiple segments.

The image segments began with:

```text
CIPB102_Lab2_Kafayat_Animashawun_USB.001
```

and continued through:

```text
CIPB102_Lab2_Kafayat_Animashawun_USB.040
```

The image therefore consists of a complete segmented Raw/DD forensic image.

### Acquisition Information

| Attribute          | Value                                |
| ------------------ | ------------------------------------ |
| Source Device      | `\\.\PHYSICALDRIVE1`                 |
| Device             | Kingston DataTraveler 3.0 USB Device |
| Image Format       | Raw/DD                               |
| Acquisition Tool   | Exterro FTK Imager 8.3.0.27          |
| Image Location     | `D:\ICDFA\CIP-B102-Lab4\`            |
| Image Segments     | `.001` – `.040`                      |
| Acquisition Start  | 30 August 2026, 19:36:38             |
| Acquisition Finish | 30 August 2026, 19:45:46             |
| Acquisition Status | Successful                           |
| Bad Blocks         | No bad blocks found                  |

The acquisition completed successfully.

### Screenshot Evidence

A screenshot showing the FTK Imager acquisition process and completion is included in the `screenshots` directory.

---

## 9. Cryptographic Hash Verification

Cryptographic hashing was used to establish and verify the integrity of the acquired forensic image.

FTK Imager calculated MD5 and SHA-1 hashes during the acquisition and verification process.

### FTK Imager Hash Results

| Hash Algorithm | Computed Hash                              | Report Hash                                | Result               |
| -------------- | ------------------------------------------ | ------------------------------------------ | -------------------- |
| MD5            | `2c6e2f1a60c49b49887dc53d2fdf092e`         | `2c6e2f1a60c49b49887dc53d2fdf092e`         | **MATCH / VERIFIED** |
| SHA-1          | `8a243d04ea4e27fe5d40ac5156500262e6bd8d74` | `8a243d04ea4e27fe5d40ac5156500262e6bd8d74` | **MATCH / VERIFIED** |

FTK Imager reported both the MD5 and SHA-1 values as verified.

The verification process also confirmed:

```text
No bad blocks found in image
```

### Verification Times

Verification started:

```text
30 August 2026 19:45:49
```

Verification finished:

```text
30 August 2026 19:49:12
```

---

## 10. SHA-256 Verification

An additional SHA-256 calculation was performed using Windows PowerShell.

The following command was used:

```powershell
Get-FileHash "D:\ICDFA\CIP-B102-Lab4\CIPB102_Lab2_Kafayat_Animashawun_USB.001" -Algorithm SHA256
```

The resulting SHA-256 value was:

```text
14DF4D66849835BD29E20EF5502841AC2C79FC68CACE3E00B3B991592D7EA96B
```

### SHA-256 Result

| Item                          | Hash Algorithm | Hash Value                                                         |
| ----------------------------- | -------------- | ------------------------------------------------------------------ |
| Forensic Image Segment `.001` | SHA-256        | `14DF4D66849835BD29E20EF5502841AC2C79FC68CACE3E00B3B991592D7EA96B` |

The SHA-256 value above represents the hash of the **`.001` image segment specifically**.

The complete Raw/DD forensic image consists of multiple segments from `.001` through `.040`. Therefore, the SHA-256 value is documented as the hash of the first image segment and is not represented as the SHA-256 hash of the complete segmented image.

This provides an additional cryptographic integrity value alongside the MD5 and SHA-1 verification performed by FTK Imager.

### Screenshot Evidence

A screenshot showing the PowerShell SHA-256 calculation is included in the `screenshots` directory.

---

## 11. Image Verification

FTK Imager successfully verified the forensic image after acquisition.

The MD5 verification produced the following result:

```text
MD5 Computed Hash:
2c6e2f1a60c49b49887dc53d2fdf092e

MD5 Report Hash:
2c6e2f1a60c49b49887dc53d2fdf092e

Result:
MATCH / VERIFIED
```

The SHA-1 verification produced:

```text
SHA-1 Computed Hash:
8a243d04ea4e27fe5d40ac5156500262e6bd8d74

SHA-1 Report Hash:
8a243d04ea4e27fe5d40ac5156500262e6bd8d74

Result:
MATCH / VERIFIED
```

FTK Imager also reported:

```text
No bad blocks found in image
```

These results demonstrate that the acquired forensic image successfully passed FTK Imager's built-in verification process.

---

## 12. Evidence File Verification

The acquired forensic image was opened and examined using FTK Imager.

The evidence tree showed the following folder:

```text
CIP-B102-Lab4-Evidence
```

The expected evidence file was located within the folder:

```text
kafayat_animashawun.txt
```

FTK Imager displayed the file as a regular file with a size of approximately 384 bytes.

### Verification Result

**Evidence File Found: YES**

The expected evidence file was successfully located within the acquired forensic image.

This confirms that the forensic image contains the evidence file created during the preparation stage.

### Screenshot Evidence

A screenshot showing `kafayat_animashawun.txt` inside the acquired forensic image is included in the `screenshots` directory.

---

## 13. Image Segment Structure

Because the Raw/DD image was segmented, the acquisition directory contains multiple image segments.

The image structure is:

```text
CIPB102_Lab2_Kafayat_Animashawun_USB.001
CIPB102_Lab2_Kafayat_Animashawun_USB.002
CIPB102_Lab2_Kafayat_Animashawun_USB.003
...
CIPB102_Lab2_Kafayat_Animashawun_USB.039
CIPB102_Lab2_Kafayat_Animashawun_USB.040
```

The `.001` file is the first segment and `.040` is the final segment.

The FTK Imager report records the complete segment list and acquisition information.

All image segments should be retained together because they collectively represent the complete forensic image.

---

## 14. Screenshots and Supporting Evidence

Screenshots were captured throughout the practical exercise to document the major stages of the forensic process.

The supporting evidence includes screenshots relating to:

1. USB evidence folder creation.
2. Evidence file creation.
3. Contents of the student-created evidence file.
4. USB device identification.
5. FTK Imager source selection.
6. Forensic image acquisition.
7. Image completion.
8. Image verification.
9. Hash verification.
10. Evidence file located within the acquired image.
11. PowerShell SHA-256 calculation.

The screenshots are stored in:

```text
screenshots/
```

---

## 15. Repository Structure

The GitHub repository is organised as follows:

```text
CIP-B102-Lab4-Forensic-USB-Acquisition/
│
├── README.md
│
├── report/
│   └── CIP-B102-Lab4-Forensic-USB-Acquisition-Report.pdf
│
├── screenshots/
│   ├── Evidence of folder creation.png
│   ├── Evidence of text file creation.png
│   ├── Text file content.png
│   ├── 04-usb-identification.png
│   ├── 05-forensic-acquisition.png
│   ├── 06-hash-verification.png
│   ├── 07-evidence-file-in-image.png
│   └── 08-sha256-powershell.png
│
└── hash-results.txt
```

The screenshot filenames above should correspond to the actual files uploaded to the repository.

If `hash-results.txt` is not included in the repository, this file should be removed from the structure shown above.

---

## 16. Chain of Custody

The following simplified chain-of-custody record documents the major stages of the laboratory exercise.

| Date/Time        | Action                | Person                      | Evidence ID | Notes                                                |
| ---------------- | --------------------- | --------------------------- | ----------- | ---------------------------------------------------- |
| 30/08/2026       | Evidence prepared     | Kafayat Omolara Animashawun | 001         | Test USB prepared for controlled laboratory exercise |
| 30/08/2026 19:36 | Evidence acquired     | Kafayat Omolara Animashawun | 001         | Physical USB acquired using FTK Imager               |
| 30/08/2026 19:45 | Acquisition completed | Kafayat Omolara Animashawun | 001         | Raw/DD forensic image successfully created           |
| 30/08/2026 19:49 | Integrity verified    | Kafayat Omolara Animashawun | 001         | MD5 and SHA-1 verification completed successfully    |

---

## 17. Findings

The following findings were obtained during the practical exercise:

* The submitted USB device was successfully identified as a **Kingston DataTraveler 3.0 USB Device**.
* The source device was identified as `\\.\PHYSICALDRIVE1`.
* The device had a reported source data size of **59006 MB**.
* The USB used the **FAT32** file system.
* The USB was successfully acquired using **Exterro FTK Imager 8.3.0.27**.
* The acquisition was performed using the **Raw/DD** image format.
* The forensic image was stored separately from the source USB.
* The resulting forensic image consisted of segments `.001` through `.040`.
* FTK Imager reported **no bad blocks found in image**.
* The MD5 computed hash matched the corresponding report hash.
* The SHA-1 computed hash matched the corresponding report hash.
* The expected evidence file `kafayat_animashawun.txt` was successfully located within the acquired forensic image.
* A SHA-256 hash was independently calculated for the `.001` image segment using Windows PowerShell.
* The SHA-256 value for the `.001` segment was `14DF4D66849835BD29E20EF5502841AC2C79FC68CACE3E00B3B991592D7EA96B`.

Overall, the acquisition and FTK Imager verification processes completed successfully.

---

## 18. Evidence Integrity

Evidence integrity is a fundamental requirement in digital forensics.

Cryptographic hashing provides a mechanism for detecting changes to digital evidence. During this practical, FTK Imager calculated MD5 and SHA-1 values and subsequently compared the computed values with the corresponding report values.

The results were:

### MD5

```text
2c6e2f1a60c49b49887dc53d2fdf092e
```

**Result: MATCH / VERIFIED**

### SHA-1

```text
8a243d04ea4e27fe5d40ac5156500262e6bd8d74
```

**Result: MATCH / VERIFIED**

### SHA-256

```text
14DF4D66849835BD29E20EF5502841AC2C79FC68CACE3E00B3B991592D7EA96B
```

**Result: Calculated for image segment `.001`**

The matching MD5 and SHA-1 values and successful FTK Imager verification support the integrity of the acquired forensic image.

The SHA-256 value provides an additional cryptographic record for the first image segment.

The original USB should be preserved separately, while subsequent examination should be conducted using the forensic image where possible.

---

## 19. Ethical and Forensic Considerations

The examination was performed for educational and forensic training purposes using a controlled test USB device.

The following forensic principles were observed:

* Only an approved test USB was used.
* The correct physical device was identified before acquisition.
* The source device was not intentionally modified during acquisition.
* The forensic image was stored separately from the source USB.
* Cryptographic hashes were used to support integrity verification.
* The forensic image was verified after acquisition.
* The expected evidence file was confirmed within the acquired image.
* Supporting screenshots and acquisition documentation were retained.
* The segmented forensic image should be kept together to preserve the complete evidence set.
* Access to forensic evidence should be controlled and documented.

---

## 20. Conclusion

This practical exercise demonstrated the fundamental principles of forensic USB acquisition and evidence integrity verification.

The Kingston DataTraveler USB was successfully identified and documented before acquisition. A physical forensic image was created using Exterro FTK Imager 8.3.0.27 in Raw/DD format and stored separately from the source device.

The resulting image was segmented into multiple files and successfully verified by FTK Imager. The MD5 and SHA-1 computed hashes matched their corresponding report hashes, and FTK Imager reported that no bad blocks were found in the image.

The expected evidence file, `kafayat_animashawun.txt`, was successfully located within the acquired forensic image.

An additional SHA-256 hash was calculated using Windows PowerShell for the `.001` image segment, producing:

```text
14DF4D66849835BD29E20EF5502841AC2C79FC68CACE3E00B3B991592D7EA96B
```

The exercise demonstrates a repeatable forensic workflow:

```text
Evidence Preparation
        ↓
Evidence Identification
        ↓
Forensic Acquisition
        ↓
Hash Calculation
        ↓
Image Verification
        ↓
Evidence File Validation
        ↓
Documentation
```

The results demonstrate the importance of correctly identifying the source device, preserving the original evidence, creating a verified forensic copy, using cryptographic hashes to support integrity, and maintaining appropriate documentation throughout the examination.

---

## 21. Declaration

I confirm that the procedures documented in this repository represent the forensic USB acquisition and verification activities performed during this practical laboratory exercise.

**Examiner:** Kafayat Omolara Animashawun

**Student ID:** 2025/FWSD/11317

**Case/Lab ID:** SBT-DF202-Lab2

**Date:** 30 August 2026

---

## 22. Submission

This repository contains the documentation and supporting evidence associated with the forensic USB acquisition and hash verification laboratory exercise.

The submission demonstrates:

**Identification → Evidence Preparation → Acquisition → Hashing → Verification → Evidence Confirmation → Documentation**

The repository contains the final forensic report and supporting screenshots documenting the major stages of the practical exercise.

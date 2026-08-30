# Lab 4 – Forensic USB Acquisition and Evidence Integrity

## 1. Overview

This practical lab demonstrates the forensic acquisition and verification of evidence from a USB flash drive using an approved forensic imaging method.

The objective of the exercise is to demonstrate the ability to:

* Identify and document a USB storage device submitted as digital evidence.
* Acquire a forensic image of the USB drive without altering the original evidence.
* Calculate cryptographic hashes of the source evidence and acquired forensic image.
* Compare the calculated hashes to verify evidence integrity.
* Confirm the presence of the expected evidence file within the acquired image.
* Document the acquisition process in a repeatable and forensically sound manner.
* Maintain appropriate documentation of the evidence and acquisition process.

---

## 2. Practical Scenario

A USB flash drive was submitted for forensic examination.

The USB device was treated as digital evidence, and the examination was performed using a controlled forensic acquisition process. The original evidence was not intentionally modified during the examination.

A forensic image of the USB device was created for analysis. Cryptographic hashing was then used to verify that the acquired image accurately represented the original evidence.

---

## 3. Objectives

The objectives of this practical exercise were to:

1. Identify the submitted USB evidence.
2. Record relevant evidence information.
3. Acquire a forensic image of the USB device.
4. Calculate cryptographic hashes.
5. Verify the integrity of the acquired forensic image.
6. Locate and confirm the expected evidence file.
7. Preserve supporting screenshots and documentation.
8. Produce a repeatable forensic acquisition report.

---

## 4. Evidence Information

| Evidence Attribute  | Details                     |
| ------------------- | --------------------------- |
| Evidence Type       | USB Flash Drive             |
| Evidence ID         | [ENTER EVIDENCE ID]         |
| Device Manufacturer | [ENTER MANUFACTURER]        |
| Device Model        | [ENTER MODEL]               |
| Serial Number       | [ENTER SERIAL NUMBER]       |
| Storage Capacity    | [ENTER CAPACITY]            |
| File System         | [ENTER FILE SYSTEM]         |
| Acquisition Date    | [ENTER DATE]                |
| Acquisition Time    | [ENTER TIME]                |
| Examiner            | Kafayat Omolara Animashawun |
| Host System         | [ENTER HOST COMPUTER]       |
| Operating System    | [ENTER OPERATING SYSTEM]    |
| Acquisition Tool    | [ENTER TOOL USED]           |
| Image Format        | [ENTER IMAGE FORMAT]        |

> **Note:** Replace all `[ENTER ...]` fields with the actual information obtained during the practical exercise.

---

## 5. Tools Used

The following tools were used during the forensic acquisition and verification process:

* [ENTER FORENSIC ACQUISITION TOOL]
* [ENTER HASHING TOOL]
* Windows Command Prompt / PowerShell, where applicable
* GitHub for evidence documentation and submission

The exact versions of the forensic tools used should be recorded in the final forensic report where available.

---

## 6. Forensic Acquisition Method

The USB flash drive was treated as the original evidence source.

The acquisition process followed these general steps:

1. Connected and identified the USB storage device.
2. Recorded relevant device information.
3. Confirmed the correct source device before acquisition.
4. Created a forensic image of the USB device.
5. Calculated cryptographic hash values.
6. Calculated the corresponding hash value for the acquired image.
7. Compared the hash values.
8. Verified that the expected evidence file was present.
9. Preserved screenshots and acquisition results as supporting documentation.

The forensic image was used for subsequent examination rather than modifying or working directly on the original USB evidence.

---

## 7. Evidence Identification

Before acquisition, the USB device was identified and its relevant characteristics were documented.

The identification process included:

* Device name and/or model
* Storage capacity
* Serial number, where available
* Device identifier
* File system
* Partition information
* Drive letter, where applicable

A screenshot documenting the identification of the USB device is included in the `screenshots` directory.

---

## 8. Forensic Image Acquisition

A forensic image of the USB flash drive was created using the approved acquisition tool.

The acquired image represents a forensic copy of the source storage device and was retained for analysis and verification.

### Image Information

| Attribute             | Value                  |
| --------------------- | ---------------------- |
| Source Device         | [ENTER SOURCE DEVICE]  |
| Image File            | [ENTER IMAGE FILENAME] |
| Image Format          | [ENTER FORMAT]         |
| Image Size            | [ENTER SIZE]           |
| Acquisition Tool      | [ENTER TOOL]           |
| Acquisition Date/Time | [ENTER DATE AND TIME]  |
| Acquisition Status    | [SUCCESS/FAILURE]      |

A screenshot of the acquisition process is included in the `screenshots` directory.

---

## 9. Cryptographic Hash Verification

Cryptographic hashes were calculated to establish and verify the integrity of the evidence.

The hash values provide a digital fingerprint that can be used to determine whether the acquired evidence has changed.

The hash algorithm(s) used during this practical were:

* [MD5, if used]
* [SHA-1, if used]
* [SHA-256, if used]

### Hash Results

| Evidence       | Hash Algorithm | Hash Value     |
| -------------- | -------------- | -------------- |
| Original USB   | [ALGORITHM]    | `[ENTER HASH]` |
| Forensic Image | [ALGORITHM]    | `[ENTER HASH]` |

### Integrity Result

**Hash Match:** [YES / NO]

If the hash calculated from the original evidence matches the corresponding hash calculated from the forensic image, the acquisition can be considered successfully verified for integrity using that hash value.

Example:

```text
Original USB Hash:    [HASH VALUE]
Forensic Image Hash:  [HASH VALUE]

Result: MATCH
```

The actual hash values obtained during the practical exercise should be inserted above.

---

## 10. Evidence File Verification

The acquired forensic image was examined to confirm the presence of the expected evidence file.

### Expected Evidence File

```text
[ENTER EXPECTED FILENAME]
```

### Verification Result

**Evidence File Found:** [YES / NO]

The evidence file was located within the acquired image at:

```text
[ENTER PATH / LOCATION]
```

A screenshot demonstrating the presence of the expected evidence file is included in the `screenshots` directory.

---

## 11. Repository Structure

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
│   ├── 01-usb-evidence.png
│   ├── 02-evidence-file.png
│   ├── 03-usb-identification.png
│   ├── 04-forensic-acquisition.png
│   ├── 05-hash-calculation.png
│   └── 06-hash-verification.png
│
└── hash-results.txt
```

> File names may be adjusted to match the actual files submitted to the repository.

---

## 12. Screenshots and Supporting Evidence

Screenshots are included to provide visual evidence of the practical activities performed.

The screenshots may include:

1. USB device identification
2. Evidence file identification
3. Source device information
4. Forensic image acquisition
5. Hash calculation
6. Hash comparison
7. Evidence integrity verification

Each screenshot should be clearly named and correspond to a documented stage of the acquisition process.

---

## 13. Evidence Integrity

Evidence integrity is a critical requirement in digital forensic investigations.

The use of cryptographic hashing provides a mechanism for demonstrating that the acquired forensic image has not been unintentionally altered.

The original evidence should be preserved separately from the working forensic image, and subsequent analysis should be performed on the forensic copy.

Where the calculated source and image hashes match, the results support the conclusion that the acquired image is an accurate and verified copy of the source evidence.

---

## 14. Chain of Custody

The evidence should be handled and documented in a manner that supports traceability throughout the examination.

The following information should be recorded where applicable:

| Date/Time   | Action             | Person                      | Evidence ID | Notes                        |
| ----------- | ------------------ | --------------------------- | ----------- | ---------------------------- |
| [DATE/TIME] | Evidence received  | Kafayat Omolara Animashawun | [ID]        | USB received for examination |
| [DATE/TIME] | Evidence acquired  | Kafayat Omolara Animashawun | [ID]        | Forensic image created       |
| [DATE/TIME] | Integrity verified | Kafayat Omolara Animashawun | [ID]        | Hash comparison completed    |

---

## 15. Findings

The following findings were obtained during the practical exercise:

* The submitted USB device was successfully identified.
* A forensic image was successfully created using the selected acquisition method.
* Cryptographic hash values were calculated.
* The hash values of the source and acquired image were [MATCHING / NOT MATCHING].
* The expected evidence file was [FOUND / NOT FOUND].
* Supporting screenshots were captured and preserved as part of the laboratory evidence.

---

## 16. Conclusion

The forensic USB acquisition exercise demonstrated the fundamental principles of digital evidence acquisition and integrity verification.

The USB flash drive was identified and documented before acquisition. A forensic image was subsequently created using an approved acquisition method. Cryptographic hashing was used to verify the integrity of the acquired image, and the expected evidence file was checked within the acquired evidence.

The process provides a repeatable approach for acquiring and validating digital evidence while reducing the risk of accidental modification to the original evidence.

---

## 17. Ethical and Forensic Considerations

The examination was conducted for educational and forensic training purposes.

Digital evidence should be handled carefully to preserve its integrity and maintain an auditable record of actions performed during an examination.

Important considerations include:

* Do not modify the original evidence unnecessarily.
* Verify the correct source device before acquisition.
* Maintain accurate evidence documentation.
* Use cryptographic hashes to support integrity verification.
* Perform analysis on forensic copies where possible.
* Maintain appropriate chain-of-custody records.
* Ensure that evidence is stored securely and access is controlled.

---

## 18. Declaration

I confirm that the procedures documented in this repository represent the forensic USB acquisition and verification activities performed during this practical exercise.

**Examiner:** Kafayat Omolara Animashawun

**Date:** [ENTER DATE]

---

## 19. Submission

This repository contains the documentation and supporting evidence associated with the Lab 4 forensic USB acquisition exercise.

The repository is intended to demonstrate:

**Identification → Acquisition → Hashing → Verification → Evidence Confirmation → Documentation**

---

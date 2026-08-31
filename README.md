# Digital Forensics Case Handling, Autopsy and Sleuth Kit Analysis

**Course:** SBT-DF202: Computer and Digital Forensics
**Practical Lab:** Lab 1
**Platform:** Windows Forensic Workstation + Autopsy 4.23.1 + The Sleuth Kit 4.14.0
**Evidence Image:** `Ch01InChap01.dd`
**Student:** Kafayat Omolara Animashawun
**Date of Examination:** 30–31 August 2026

---

## 1. Practical Overview

This practical laboratory demonstrates the application of digital forensic investigation procedures using **Autopsy** and **The Sleuth Kit**.

The investigation involved the examination of the authorised ICDFA training forensic disk image `Ch01InChap01.dd`.

The objectives were to preserve evidence integrity, identify deleted files, perform keyword searches, analyse filesystem and file metadata, recover relevant evidence, verify recovered evidence using cryptographic hashes, and document the investigation using a repeatable forensic methodology.

The original forensic image was preserved throughout the investigation and was not intentionally modified. All recovered files, screenshots, reports and analysis outputs were stored separately from the original evidence.

---

## 2. Objectives

The practical objectives were to:

* Preserve and verify the integrity of the forensic disk image.
* Calculate and document MD5 and SHA-256 hashes.
* Maintain a mini chain-of-custody/evidence worksheet.
* Create and configure a forensic case in Autopsy.
* Examine the forensic image using Autopsy.
* Identify deleted files.
* Perform keyword searches.
* Tag and recover relevant evidence.
* Generate an Autopsy forensic report.
* Analyse the image using The Sleuth Kit command-line tools.
* Use `img_stat`, `mmls`, `fsstat`, `fls`, `istat`, `icat`, `blkcat`, `blkls` and `tsk_recover`.
* Identify the metadata address of `INCOME.XLS`.
* Examine file metadata and data units using `istat`.
* Recover `INCOME.XLS` using `icat`.
* Perform block-level recovery using `blkcat` where applicable.
* Perform additional recovery using `tsk_recover`.
* Calculate and compare cryptographic hashes of recovered files.
* Examine the recovered spreadsheet locally.
* Produce a professional forensic report supported by screenshots and evidence.

---

## 3. Evidence Information

| Evidence Detail              | Result                                                             |
| ---------------------------- | ------------------------------------------------------------------ |
| **Evidence filename**        | `Ch01InChap01.dd`                                                  |
| **Evidence type**            | Forensic disk image                                                |
| **Evidence source**          | Authorised ICDFA training forensic image                           |
| **Original location**        | `D:\Lab1_Digital_Forensics\Original_Evidence\Ch01InChap01.dd`      |
| **File size**                | 1,474,560 bytes (1.40 MB)                                          |
| **MD5**                      | `A117773BCF1FC88EC0AB8E0A349FBBCB`                                 |
| **SHA-256**                  | `3CE8053E4F3D9C8AB98B3AADB2480685EFB8E4980D34297B83BD5A09B1A7B122` |
| **Date received/downloaded** | 30 August 2026                                                     |
| **Original image modified**  | No                                                                 |
| **Evidence status**          | Original forensic image — preserved                                |

---

## 4. Tools Used

The following tools were used during the investigation:

### Forensic Analysis

* **Autopsy 4.23.1**
* **The Sleuth Kit 4.14.0**

### Sleuth Kit Utilities

```text
img_stat
mmls
fsstat
fls
istat
icat
blkcat
blkls
tsk_recover
```

### Windows Utilities

PowerShell was used for file management, command execution and cryptographic hashing.

The Windows `Get-FileHash` command was used to calculate MD5 and SHA-256 hashes where applicable.

---

## 5. Investigation Methodology

The investigation followed a structured forensic workflow:

1. Evidence identification and preservation.
2. Evidence file size verification.
3. MD5 and SHA-256 hash calculation.
4. Chain-of-custody documentation.
5. Autopsy case creation.
6. Addition of the forensic image as an evidence source.
7. Autopsy ingest processing.
8. Deleted-file examination.
9. Keyword searching.
10. Evidence identification and tagging.
11. Autopsy report generation.
12. Sleuth Kit image examination.
13. Filesystem analysis.
14. File and deleted-file listing.
15. Identification of `INCOME.XLS`.
16. Metadata examination using `istat`.
17. Recovery using `icat`.
18. Block-level examination/recovery using `blkcat` where applicable.
19. Additional recovery using `tsk_recover`.
20. Cryptographic hash comparison.
21. Local examination of recovered evidence.
22. Documentation of findings and preparation of the forensic report.

---

# 6. Evidence Integrity

Cryptographic hashes were calculated for the original forensic image before forensic examination.

### Original Evidence Hashes

**MD5**

```text
A117773BCF1FC88EC0AB8E0A349FBBCB
```

**SHA-256**

```text
3CE8053E4F3D9C8AB98B3AADB2480685EFB8E4980D34297B83BD5A09B1A7B122
```

The original image was maintained in:

```text
D:\Lab1_Digital_Forensics\Original_Evidence\
```

The source image was not modified during the investigation. Recovered files and analysis outputs were stored in separate working directories.

---

# 7. Chain of Custody

A mini chain-of-custody/evidence worksheet was created for the forensic image.

The worksheet documented:

* Case identification
* Evidence identification
* Evidence description
* Evidence source
* Original storage location
* File size
* MD5 hash
* SHA-256 hash
* Examiner
* Evidence status
* Handling and examination activities

The original evidence was maintained separately from recovered files and analysis outputs.

The completed chain-of-custody documentation is stored in:

```text
/chain_of_custody/
```

---

# 8. Autopsy Analysis

Autopsy 4.23.1 was used to create and analyse the forensic case.

### Case

The case was created as:

```text
ICDFA_SBT_DF202_Lab1
```

The authorised forensic image was added as the evidence source:

```text
Ch01InChap01.dd
```

The image was analysed using Autopsy's filesystem and ingest capabilities.

---

## 8.1 Deleted File Analysis

The Autopsy analysis identified six entries in the Deleted Files view, including:

```text
Billing Letter.doc
confirmation.txt
letter1.txt
Regrets.doc
f0000000_13_October_2003.doc
f0000049_02_November_2003.doc
```

The Autopsy results identified the relevant entries as unallocated/carved evidence.

The deleted-file analysis was documented using screenshots.

---

## 8.2 Keyword Search

Keyword searching was performed in Autopsy.

A keyword search for **Laura Roper** returned three relevant results:

```text
f0000000_13_October_2003.doc
Billing Letter.doc
Income.xls
```

The search results demonstrated that the keyword was present in both recovered/carved evidence and the active `Income.xls` file.

The keyword-search results were preserved through screenshots and the generated Autopsy report.

---

## 8.3 Evidence Tagging and Reporting

Relevant evidence was identified during the Autopsy examination and the required reporting functionality was used.

An HTML Autopsy report was generated to preserve the results of the examination.

The generated report included relevant examination results such as keyword hits and verification information.

Autopsy screenshots and supporting outputs are stored in:

```text
/screenshots/autopsy/
```

Autopsy-generated reports are stored in:

```text
/autopsy/
```

---

# 9. Sleuth Kit Analysis

The forensic image was examined using **The Sleuth Kit 4.14.0** command-line tools on Windows.

The following utilities were used:

```text
img_stat
mmls
fsstat
fls
istat
icat
blkcat
blkls
tsk_recover
```

---

## 9.1 Image Analysis — `img_stat`

The `img_stat` utility was used to obtain basic information about the forensic image.

The command confirmed information about the image format and characteristics.

Supporting evidence is stored in:

```text
/screenshots/sleuthkit/
```

---

## 9.2 Volume Analysis — `mmls`

The `mmls` utility was executed to examine the image for partition information.

The image did not return a conventional partition table requiring a non-zero partition offset for filesystem analysis.

The subsequent filesystem analysis confirmed that the filesystem begins at sector offset:

```text
0
```

---

## 9.3 Filesystem Analysis — `fsstat`

`fsstat` was executed using an offset of zero:

```text
fsstat -o 0 Ch01InChap01.dd
```

The filesystem was identified as:

```text
FAT12
```

Important filesystem characteristics included:

| Property                  | Result    |
| ------------------------- | --------- |
| File system type          | FAT12     |
| Sector size               | 512 bytes |
| Cluster size              | 512 bytes |
| Sectors before filesystem | 0         |
| Total sector range        | 0–2879    |
| Data area                 | 19–2879   |
| Root directory            | 19–32     |
| Cluster area              | 33–2879   |

This confirmed that filesystem analysis could be performed using an image offset of `0`.

---

# 10. Deleted File Analysis Using `fls`

The `fls` command was used to list files within the filesystem.

The initial listing identified:

```text
Client Info.mdb
Billing Letter.doc
confirmation.txt
Income.xls
letter1.txt
Regrets.doc
```

The Sleuth Kit output marked several files with an asterisk, indicating unallocated/deleted entries.

The recursive deleted-file listing identified:

```text
Billing Letter.doc
confirmation.txt
letter1.txt
Regrets.doc
```

These results were consistent with the deleted-file findings observed in Autopsy.

---

# 11. INCOME.XLS Identification

The `fls` recursive search was used to locate `Income.xls`.

The command returned:

```text
r/r 13: Income.xls
```

Therefore, the metadata address associated with the file was identified as:

```text
Metadata Address: 13
```

The file was listed without the deleted/unallocated marker, indicating that `Income.xls` was an allocated file in the filesystem.

---

# 12. INCOME.XLS Metadata Analysis

The `istat` utility was used to examine metadata address `13`.

The analysis provided information about the file, including its metadata and data-unit allocation.

The data units identified for `Income.xls` were:

```text
301
302
303
304
305
306
307
308
309
310
311
```

Therefore, the file occupied data units **301–311**.

The `istat` output was captured and retained as supporting forensic evidence.

---

# 13. INCOME.XLS Recovery Using `icat`

The `icat` utility was used to recover `Income.xls` using its metadata address.

The recovery command used the confirmed filesystem offset of `0` and metadata address `13`.

The recovered file was stored separately from the original evidence in:

```text
D:\Lab1_Digital_Forensics\Recovered\SleuthKit\
```

The recovered file was named:

```text
INCOME_icat.xls
```

The original forensic image remained untouched during this recovery process.

---

# 14. Block-Level Analysis Using `blkcat`

The `istat` results identified data units 301–311 associated with `Income.xls`.

These data units were used for the required block-level analysis/recovery using `blkcat`, where applicable.

The purpose of this step was to demonstrate direct examination of the filesystem data units associated with the target file and to provide an additional recovery method for comparison.

Supporting command output and screenshots are stored in:

```text
/sleuthkit/
```

---

# 15. Block Data Examination Using `blkls`

The `blkls` utility was used to extract filesystem block data where required by the practical.

The extracted output was stored separately from the original evidence image.

This activity supported examination of filesystem block-level information without modifying the source forensic image.

---

# 16. File Recovery Using `tsk_recover`

The `tsk_recover` utility was used to perform additional filesystem recovery.

Recovered files were stored in a dedicated recovery directory separate from the original forensic image:

```text
D:\Lab1_Digital_Forensics\Recovered\TSK_Recover\
```

This provided an independent recovery method for comparison with the `icat` recovery.

---

# 17. Cryptographic Hash Verification

Cryptographic hashes were calculated for recovered evidence to support integrity verification and comparison between recovery methods.

The recovery methods considered included:

| Recovery Method | File                         |
| --------------- | ---------------------------- |
| `icat`          | `INCOME_icat.xls`            |
| `blkcat`        | Block-level recovered output |
| `tsk_recover`   | Recovered filesystem copy    |

The final MD5 and SHA-256 results for each recovered copy were documented in the forensic report and supporting hash evidence.

Where recovered copies produced matching cryptographic hashes, this provided evidence that the recovery methods produced identical file content.

---

# 18. Local Examination of Recovered Spreadsheet

The recovered spreadsheet was examined locally to confirm successful recovery and to verify that its contents were accessible.

The spreadsheet contained financial information including a January cash-flow table.

The recovered content included entries such as:

* Laura Roper
* Earnest Bell
* Frank Haron
* Thomas George
* Randall Watson

The January table included income, setup, contact and total values, with a recorded grand total of:

```text
$3,945.00
```

The spreadsheet metadata also identified:

```text
Creator: Amelia Phillips
Application: Microsoft Excel
Company: Starships CMS
Created: 23 November 2002
Modified: 9 December 2005
```

These observations were used to demonstrate successful examination of the recovered spreadsheet.

---

# 19. Errors and Corrective Actions

During the command-line examination, an `fsstat` command was initially executed without specifying an offset value, resulting in an invalid argument error.

The command was corrected by explicitly specifying the confirmed filesystem offset:

```text
-o 0
```

A subsequent `fsstat` execution successfully identified the filesystem as FAT12.

During the initial `icat` recovery attempt, the output directory did not exist. The recovery command therefore produced a Windows path error.

The issue was identified as a working-directory/output-path problem rather than an evidence-integrity problem. A dedicated recovery directory was created before repeating the recovery operation.

These corrective actions were documented to maintain a repeatable forensic workflow.

---

# 20. Screenshots and Supporting Evidence

Screenshots were captured throughout the investigation to demonstrate the major stages of the practical.

The evidence includes screenshots covering:

* Evidence image information
* Original evidence hashes
* Chain of custody
* Autopsy case creation
* Evidence source configuration
* Autopsy deleted-file listing
* Keyword-search results
* Tagged/recovered evidence
* Autopsy report generation
* `img_stat`
* `mmls`
* `fsstat`
* `fls`
* Recursive deleted-file listing
* `INCOME.XLS` identification
* `istat`
* `icat`
* `blkcat`
* `blkls`
* `tsk_recover`
* Hash comparison
* Local examination of the recovered spreadsheet

Screenshots are organised under:

```text
/screenshots/
```

---

# 21. Repository Structure

The repository is organised as follows:

```text
Lab1-Digital-Forensics-Autopsy-SleuthKit/
│
├── README.md
│
├── screenshots/
│   ├── autopsy/
│   └── sleuthkit/
│
├── evidence/
│
├── autopsy/
│
├── sleuthkit/
│
├── recovered_files/
│
├── hashes/
│
├── chain_of_custody/
│
└── report/
```

The folders are used to separate evidence documentation, forensic analysis outputs, recovered files, screenshots and reporting materials.

---

# 22. Forensic Handling Statement

The authorised ICDFA training forensic image was treated as original evidence throughout the investigation.

The original image:

```text
Ch01InChap01.dd
```

was preserved and was not intentionally modified.

The original image was stored separately from:

* Recovered files
* Screenshots
* Autopsy reports
* Sleuth Kit outputs
* Hash records
* Chain-of-custody documentation
* Final forensic report

Cryptographic hashing was used to establish and support evidence integrity.

---

# 23. Final Findings

The investigation successfully demonstrated the use of both Autopsy and The Sleuth Kit for forensic examination of the authorised training image.

Key findings included:

1. The evidence image was successfully preserved and its original MD5 and SHA-256 hashes were documented.

2. The filesystem was identified as **FAT12**.

3. The filesystem analysis was performed using an image offset of **0 sectors**.

4. Deleted files were identified using both Autopsy and Sleuth Kit analysis.

5. The deleted files identified through Sleuth Kit included:

   * `Billing Letter.doc`
   * `confirmation.txt`
   * `letter1.txt`
   * `Regrets.doc`

6. `Income.xls` was identified at metadata address **13**.

7. `istat` identified data units **301–311** for `Income.xls`.

8. `Income.xls` was successfully targeted for recovery using `icat`.

9. Additional recovery and block-level analysis were performed using the required Sleuth Kit utilities.

10. Keyword searching in Autopsy for **Laura Roper** produced three relevant results:

* `f0000000_13_October_2003.doc`
* `Billing Letter.doc`
* `Income.xls`

11. The recovered spreadsheet was successfully examined and contained January cash-flow information.

12. The forensic workflow, commands, outputs, errors and corrective actions were documented using screenshots and supporting evidence.

---

# 24. Conclusion

This practical demonstrated the application of a structured digital forensic investigation methodology using Autopsy and The Sleuth Kit.

The investigation successfully covered evidence preservation, cryptographic hashing, chain-of-custody documentation, filesystem examination, deleted-file identification, keyword searching, metadata analysis and file recovery.

The use of both graphical and command-line forensic tools provided complementary methods of examining the evidence. Autopsy facilitated structured case management, keyword searching, evidence review and reporting, while The Sleuth Kit provided lower-level filesystem and metadata analysis.

The identification of the FAT12 filesystem, determination of the correct filesystem offset, identification of `Income.xls` at metadata address 13, examination of its metadata and identification of data units 301–311 demonstrated practical understanding of filesystem-level forensic analysis.

The recovery and examination activities were performed separately from the original forensic image, supporting evidence preservation and repeatability.

Overall, the laboratory objectives were achieved, and the exercise provided practical experience in handling forensic evidence, conducting filesystem analysis, recovering digital artefacts and documenting findings in a professional and reproducible manner.

---

## 25. Submission Note

The original `Ch01InChap01.dd` forensic image is **not included in this repository**, in accordance with the laboratory requirement that the original DD image should not be submitted unless specifically requested by the instructor.

The repository contains the supporting documentation, screenshots, forensic outputs, recovered evidence and final report required to demonstrate completion of the practical.

---

**Author:** Kafayat Omolara Animashawun
**Student ID:** 2025/FWSD/11317
**Course:** SBT-DF20: Computer and Digital Forensics
**Practical:** Lab 1: Digital Forensics Case Handling, Autopsy and Sleuth Kit Analysis

# Digital Forensics Case B4DM755

## Room Objective

This room introduces the fundamentals of **Digital Forensics & Incident Response (DFIR)** through a practical investigation involving suspected corporate espionage and theft of trade secrets.

The room covers the responsibilities of a **DFIR First Responder**, digital evidence acquisition, **Chain of Custody**, forensic disk imaging, evidence analysis using **FTK Imager**, metadata analysis, and the process of presenting digital evidence in court.

---

## Concepts Learned

### Digital Forensics & DFIR

Digital forensics involves the acquisition, preservation, examination, and analysis of digital artefacts and evidence obtained during an investigation.

A **DFIR First Responder** is responsible for the initial acquisition and preservation of digital evidence while ensuring that its integrity is maintained.

### Chain of Custody

The **Chain of Custody** documents how evidence is collected, handled, transferred, and preserved throughout an investigation.

Important practices include:

- Properly documenting seized devices and files.
- Hashing and copying files to maintain integrity.
- Bagging, sealing, and tagging obtained artefacts.
- Verifying evidence during handover.
- Maintaining proper documentation throughout the investigation.

### Forensic Imaging

A forensic disk image is a copy of a storage device that can be analysed without directly modifying the original evidence.

**Hash verification** can be used to confirm that the forensic image corresponds to the original physical drive.

### FTK Imager

**FTK Imager** is a digital forensics tool used to acquire and analyse digital evidence while preserving its integrity.

Important interface components include:

- **Evidence Tree Pane** — displays the hierarchical structure of evidence sources.
- **File List Pane** — displays files and folders within the selected location.
- **Viewer Pane** — displays the contents of selected files.

### Metadata Analysis

File metadata can reveal useful investigative information such as:

- Actual file types.
- Device models.
- GPS coordinates.
- Other information associated with the creation or modification of an artefact.

### Digital Forensics Investigation Phases

The investigation can be divided into four main phases:

1. **Pre-search**
2. **Search**
3. **Post-search**
4. **Trial**

---

# Task 1 — Introduction

## Concepts Learned

The investigation involves **William S. McClean**, a British suspect associated with **Case #B4DM755** and suspected of corporate espionage and theft of trade secrets.

A court-issued **search warrant** was obtained before investigating the suspect and his residence.

For this scenario, the official role is **Forensics Lab Analyst**, while the assigned operational role is **DFIR First Responder**.

## Hands-on Tasks

The DFIR First Responder is responsible for gathering **digital artefacts and evidence** from the crime scene and ensuring that they are properly preserved.

## THM Questions

| Question | Answer |
|---|---|
| What is your official role? | `Forensics Lab Analyst` |
| What role was assigned to you for this specific scenario? | `DFIR First Responder` |
| What do you have to gather? | `digital artefacts and evidence` |
| What document is needed before performing any legal search? | `search warrant` |

## Key Takeaways

- Digital evidence must be properly acquired and preserved.
- A **search warrant** is required before conducting a legal search.
- The **DFIR First Responder** handles the initial acquisition of evidence.

---

# Task 2 — Case B4DM755: Details of the Crime

## Concepts Learned

Digital evidence must be handled carefully to ensure that it remains authentic and suitable for examination and potential use in litigation.

When dealing with a computer system at a crime scene, the responder should consider:

1. Taking an image of the RAM.
2. Checking for drive encryption.
3. Taking an image of the drive(s).

The **Chain of Custody** ensures accountability and helps maintain the integrity of evidence throughout its handling and transfer.

## Hands-on Tasks

Evidence should be properly documented and preserved before being transferred to the Forensics Laboratory.

Important steps include:

- Hashing and copying files.
- Bagging, sealing, and tagging artefacts.
- Verifying evidence during handover.
- Maintaining Chain of Custody documentation.

## THM Questions

| Question | Answer |
|---|---|
| Before imaging drives, what must we check them for? | `drive encryption` |
| What should be done to ensure and maintain the integrity of original files in the Chain of Custody? | `Hash and copy` |
| What must be done before sending obtained artefacts to the Forensics Laboratory? | `Bag, Seal, and Tag the obtained artefacts` |

## Key Takeaways

- Always check for **drive encryption** before imaging.
- Hashing helps maintain evidence integrity.
- Evidence must be properly **bagged, sealed, tagged, and documented**.

---

# Task 3 — Practical Application of the Digital Forensics Process

## Concepts Learned

The digital forensics process involves acquiring, preserving, verifying, and analysing digital evidence.

The original artefact should be preserved while examination is performed on a forensic copy.

## Hands-on Tasks

The practical process involves:

1. Acquiring the digital artefact.
2. Preserving and documenting the evidence.
3. Maintaining the Chain of Custody.
4. Creating a forensic image.
5. Verifying the integrity of the image.
6. Analysing the forensic image.

## Key Takeaways

- Digital evidence should be preserved before examination.
- Analysis should be performed using a **forensic copy** rather than unnecessarily modifying the original evidence.
- Documentation and integrity verification are important throughout the process.

---

# Task 4 — Case B4DM755: At the Scene of Crime

## Concepts Learned

During the search of William S. McClean's residence, a **flash drive** was discovered under the suspect's desk.

A key chain attached to the flash drive contained the initials **WSM**, suggesting that it belonged to William S. McClean.

The artefact had to be documented, labelled, preserved, and recorded using the Chain of Custody before being transported to the Forensics Laboratory.

## Hands-on Tasks

The acquired flash drive was treated as digital evidence and prepared for forensic imaging.

## THM Questions

| Question | Answer |
|---|---|
| What is the only possible artefact found in the suspect's residence? | `flash drive` |
| Based on the scenario and the previous task, what should be done with that acquired suspect artefact? | `Taking an image` |
| What is the crucial aspect of the Chain of Custody that ensures individual accountability and guarantees a transparent and untainted transfer of artefacts and evidence? | `Ensure proper documentation` |

## Key Takeaways

- Physical devices discovered during an investigation can contain important digital evidence.
- Acquired artefacts should be properly documented and preserved.
- A forensic image should be created before analysis.

---

# Task 5 — Introduction to FTK Imager

## Concepts Learned

**FTK Imager** is a digital forensics tool used to acquire and analyse computer data while preserving the authenticity and integrity of evidence.

A **write-blocking device** can prevent accidental modification of a suspect drive during acquisition.

### FTK Imager Interface

| Component | Purpose |
|---|---|
| **Evidence Tree Pane** | Displays the hierarchical structure of evidence sources. |
| **File List Pane** | Displays files and folders within the selected location. |
| **Viewer Pane** | Displays the contents of selected files. |

## Hands-on Tasks

The flash drive was loaded into FTK Imager and checked for encryption.

The attached flash drive was found to be **unencrypted**.

## THM Questions

| Question | Answer |
|---|---|
| What device will prevent tampering when acquiring a forensic disk image? | `write-blocking device` |
| What is the UI element of FTK Imager which displays a hierarchical view of the added evidence sources? | `Evidence Tree Pane` |
| Is the attached flash drive encrypted? (Y/N) | `N` |
| What is the UI element of FTK Imager which displays a list of files and folders? | `File List Pane` |

## Key Takeaways

- **FTK Imager** can be used to acquire and analyse forensic evidence.
- A **write-blocking device** helps prevent evidence modification.
- Understanding the Evidence Tree, File List, and Viewer Panes is important when navigating evidence.

---

# Task 6 — Using FTK Imager to Acquire Digital Artefacts and Evidence

## Concepts Learned

This task demonstrates the practical acquisition of a forensic disk image using FTK Imager.

The process includes checking encryption, creating a forensic image, verifying its integrity, mounting the image, and recovering deleted files.

### EFS Encryption

The flash drive was checked for **EFS encryption** using FTK Imager.

The drive was found to be **not encrypted**.

### Forensic Disk Imaging

A forensic disk image was created using the **Raw (dd)** image type.

FTK Imager was configured to:

- Verify the image after creation.
- Create directory listings.
- Record case and evidence information.

### Hash Verification

FTK Imager hashed the physical drive and forensic image.

Matching hashes provide evidence that the forensic image corresponds to the original drive.

## Hands-on Tasks

### Detecting EFS Encryption

The process involved:

1. Opening FTK Imager.
2. Selecting **File → Add Evidence Item**.
3. Choosing **Physical Drive**.
4. Selecting the Microsoft Virtual Disk.
5. Selecting **File → Detect EFS Encryption**.
6. Checking the result.

### Creating a Forensic Disk Image

The forensic image was created through:

**File → Create Disk Image → Physical Drive**

The image type selected was **Raw (dd)**.

### Mounting and Analysing the Image

The forensic image was added using:

**File → Add Evidence Item → Image File**

The evidence could then be explored through the Evidence Tree Pane, File List Pane, and Viewer Pane.

### Recovering Deleted Files

Deleted files could be recovered by selecting the relevant file or directory and using **Export Files**.


## THM Questions

| Question | Answer |
|---|---|
| What is the UI element of FTK Imager which displays the content of selected files? | `Viewer Pane` |
| Identify the FTK Imager Viewer Pane. | **Viewer Pane** |
| What is the SHA1 hash of the physical drive and forensic image? | `d82f393a67c6fc87a023b50c785a7247ab1ac395` |
| Including hidden files, how many files are currently stored on the flash drive? | `8` |
| How many files were deleted in total? | `6` |
| How many recovered files are corrupted (e.g., 0 file size)? | `3` |

Evidence:

<img width="552" height="434" alt="Screenshot 2026-08-14 173458" src="https://github.com/user-attachments/assets/8b072ec1-6846-4fe2-b5d2-905d05422450" />

## Key Takeaways

- FTK Imager can create and verify forensic disk images.
- **Raw (dd)** can be used as a forensic image format.
- Hashes can be used to verify evidence integrity.
- Deleted files may still be recoverable during forensic analysis.
- Analysis should be performed on the forensic image rather than the original evidence.

---

# Task 7 — Case B4DM755: At the Forensics Laboratory

## Concepts Learned

At the Forensics Laboratory, the acquired flash drive was examined while maintaining its authenticity and integrity.

The investigation involved:

- Verifying the Chain of Custody.
- Creating and verifying a forensic disk image.
- Preserving the original evidence.
- Analysing the forensic image.
- Examining metadata and recovered artefacts.

### Metadata Analysis

Metadata can provide information that is not immediately visible from the file itself.

The investigation revealed:

- The visible extension of the **hideout** file was `.pdf`.
- Its actual extension was `.jpg`.
- The hideout photograph was taken using a **ONEPLUS A6013**.
- The warehouse photograph was taken using a **Mi 9 Lite**.
- GPS coordinates were associated with a 2022 meetup.
- The suspect's point of contact in 2022 was **Karl Renato Abelardo**.

## Hands-on Tasks

The recovered artefacts were examined using **ExifTool** and other forensic analysis techniques.


Further analysis involved examining the contents of `pandorasbox.zip`, identifying the source of code, and finding additional information contained within the recovered documents.

## THM Questions

| Question | Answer |
|---|---|
| Aside from FTK Imager, what is the directory name of the other tool located in the tools directory under Desktop? | `exiftool-12.47` |
| What is the visible extension of the "hideout" file? | `.pdf` |
| What is the actual extension of the "hideout" file? | `.jpg` |
| What is the phone model used to photograph the "hideout"? | `ONEPLUS A6013` |
| What is the phone model used to photograph the "warehouse"? | `Mi 9 Lite` |
| Are there any indications that the suspect is involved in other illegal activity? | `Y` |
| Who was the point of contact of Mr William S. McClean in 2022? | `Karl Renato Abelardo` |
| What are the GPS coordinates during the 2022 meetup? | `14°26'25.7"N 120°59'00.8"E` |
| What is the password to extract `pandorasbox.zip`? | `DarkVault$Pandora=DONOTOPEN!K1ngCr1ms0n!` |
| From which company did the source code in the `pandorasbox` directory originate? | `SwiftSpend Financial` |
| Who was listed as the beneficiary in one of the unsigned documents? | `Mr. Giovanni Vittorio DeVentura` |
| What is the hidden flag? | `THM{sCr0LL_sCr0LL_cL1cK_cL1cK_4TT3NT10N_2_D3T41L5_15_CRUC14L!!}` |

Evidence:

<img width="703" height="259" alt="Screenshot 2026-08-14 190159" src="https://github.com/user-attachments/assets/625a016b-f13c-40f8-8f61-1043ae26d08c" />
<img width="748" height="432" alt="Screenshot 2026-08-14 190341" src="https://github.com/user-attachments/assets/1ecba180-82f9-4227-890e-281ffa3218f0" />
<img width="596" height="63" alt="Screenshot 2026-08-14 185950" src="https://github.com/user-attachments/assets/657f11e0-cc50-48f4-8c83-a31ac18eea63" />

## Key Takeaways

- File extensions cannot always be trusted when analysing digital evidence.
- **Metadata** can reveal useful investigative information.
- ExifTool can assist with extracting metadata from files.
- Deleted, hidden, or disguised information may provide important evidence during an investigation.
---

# Task 8 — Post-Analysis of Evidence to Court Proceedings

## Concepts Learned

After forensic analysis, digital evidence must remain properly documented and preserved for potential court proceedings.

The investigation consists of four main phases:

### Pre-search

Activities before the search include:

- Requesting preservation of relevant data and logs.
- Obtaining a warrant for search, seizure, and examination.
- Inspecting publicly available information.

### Search

During the search:

- Obtain requested data using the court-issued warrant.
- Perform the search, seizure, and examination of computer data.

### Post-search

After acquisition:

- Perform forensic analysis on the acquired digital evidence.

### Trial

During court proceedings:

- Present forensic artefacts and evidence together with proper documentation.

## THM Questions

| Question | Answer |
|---|---|
| In which phase is a warrant obtained for search, seizure, and examination of the suspect's computer data? | `Pre-search` |
| In which phase is forensic analysis performed on acquired digital evidence? | `Post-search` |
| Which phase involves presenting forensic artefacts and evidence with proper documentation in court? | `Trial` |
## Key Takeaways

- Digital forensic investigations continue beyond evidence acquisition and analysis.
- Evidence must remain properly documented and preserved for court.
- The main phases are **Pre-search, Search, Post-search, and Trial**.
- Proper documentation supports the authenticity and integrity of digital evidence.

---

## Key Takeaways

- **DFIR First Responders** are responsible for the initial acquisition and preservation of digital evidence.
- **Chain of Custody** maintains accountability and supports evidence integrity.
- **Write-blocking** helps prevent accidental modification of original evidence.
- Forensic analysis should be performed on a **forensic image** rather than directly on the original evidence.
- **Hash verification** helps confirm forensic image integrity.
- **FTK Imager** can be used for evidence acquisition, imaging, verification, and analysis.
- Deleted and hidden files can contain valuable forensic evidence.
- **Metadata analysis** can reveal information such as file types, device models, and GPS coordinates.
- Digital forensic investigations involve **Pre-search, Search, Post-search, and Trial** phases.
- Proper documentation and preservation are essential when digital evidence may be presented in court.

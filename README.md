
# FILE-RECOVERY-USING-AUTOPSY-SOFTWARE

## AIM
To use **Autopsy Digital Forensics Tool** to retrieve deleted files from a disk image.

---

## REQUIREMENTS
- **Operating System**: Windows 10/11, macOS, or Linux
- **Tool**: [Autopsy Digital Forensics](https://www.autopsy.com/)  
- **Test Data**: Disk image file (`disk.dd`, `disk.img`, `.E01`)

---

## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Install Autopsy]
    B --> C[Create New Case in Autopsy]
    C --> D[Add Data Source: Disk Image]
    D --> E["Run File System & Data Recovery Modules"]
    E --> F[Locate Deleted Files in Results]
    F --> G[Recover and Export Deleted Files]
```
## DESIGN STEPS:
### Step 1:
Open Autopsy and create a new case with appropriate case details.

### Step 2:
Add a disk image as a data source and let Autopsy analyze the content.

### Step 3:
Navigate to the "Deleted Files" section in Autopsy and examine or recover the deleted files.

## PROGRAM:
### Install Autopsy
```bash
# Download Autopsy from:
# https://www.autopsy.com/
# Install following the setup wizard.
```
### Create a New Case
```
# File → New Case
# Enter Case Name: Deleted_File_Recovery
# Choose Base Directory: C:\Cases\Deleted_File_Recovery
# Click Finish
```
### Add Disk Image
```
# Add Data Source → Disk Image or VM File
# Browse to: C:\forensics\disk.dd
# Click Next
```
### Run Ingest Modules
```# Select:
# - File System Analysis
# - Keyword Search (optional)
# - Data Recovery / Carving
# Click Finish
```
### Locate Deleted Files
```
# Navigate to 'Deleted Files' section in the tree view
# Review metadata (size, hash, timestamps)
```
### Export Deleted Files
```
# Right-click → Extract File(s)
# Save to: C:\forensics\Recovered_Files\
```

## OUTPUT:

<img width="1194" height="718" alt="Screenshot 2025-09-11 220122" src="https://github.com/user-attachments/assets/bf39d71f-2eec-4476-9713-c14b82f01271" />
<img width="1186" height="695" alt="Screenshot 2025-09-11 220145" src="https://github.com/user-attachments/assets/d99341dc-1ee9-4ec8-a60f-c4ebee7e36d3" />

<img width="1705" height="1009" alt="Screenshot 2025-09-12 081915" src="https://github.com/user-attachments/assets/7c8ec393-1ad0-4171-a742-b6d5e552bd9e" />

<img width="1699" height="1008" alt="Screenshot 2025-09-12 082113" src="https://github.com/user-attachments/assets/74fa3dae-1d5f-4fc0-9079-763979a762d2" />
<img width="1704" height="1011" alt="Screenshot 2025-09-12 082224" src="https://github.com/user-attachments/assets/a35249d5-14b2-439e-a91a-aaa0f22d2941" />

<img width="1704" height="1010" alt="Screenshot 2025-09-12 082306" src="https://github.com/user-attachments/assets/897d199e-c34f-4b5c-8dac-bca2f9529045" />

<img width="1704" height="1015" alt="Screenshot 2025-09-12 082643" src="https://github.com/user-attachments/assets/d7b3fe5d-86c7-456b-a5b2-a090f9487d4d" />
<img width="1849" height="995" alt="Screenshot 2025-09-12 082710" src="https://github.com/user-attachments/assets/af188e39-67a6-455f-8fa8-897fa947bd1a" />

Recovered Deleted File List and Details

## RESULT:
Deleted files were successfully retrieved and analyzed using Autopsy.

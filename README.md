# Security Lab 20: Encryption EFS

This lab focuses on exploring the Encryption File System (EFS) on Windows. It includes tasks related to configuring EFS, managing keys, creating and accessing encrypted files, and understanding the importance of strong password policies for securing EFS.

### Objectives
- Understand the file system requirements and commands for EFS usage.
- Learn to back up and restore EFS encryption keys.
- Explore password policies and their impact on accessing encrypted files.
- Install and use Personal Information Exchange (PFX) keys to recover encrypted files.

### Key Results
- **Required File System**: NTFS is required for EFS functionality.
- **Creating Users, Files, and Directories**:
  - **Create a User**: `net user jessejames cowboy /add`
  - **Create a File**: `echo 123-45-6789 > SSN.txt`
  - **Create a Directory**: `mkdir private`
- **Managing EFS Keys**:
  - Back up EFS keys via:  
    `START > Control Panel > User Accounts and Family Safety > User Accounts > Manage your File Encryption Certificates`
  - Password Changes:  
    - If the password is changed by an administrator, EFS files become inaccessible.  
    - If the user changes their password, EFS remains unaffected.  
  - Change Password Command: `net user student 123`
- **Importance of Strong Passwords**:
  - Strong passwords protect recovery keys from being compromised.
- **Recovering Files Using PFX**:
  - **Password Requirement**: A password is mandatory for PFX key installation.
  - **Default Color for EFS Files**: Green.
  - **Certificate Import Success**:
    - Confirmed via a pop-up from the Certificate Import Wizard.  
    - Verification by opening the encrypted file.  
  - **PFX Definition**: Personal Information Exchange.

### Recommendations
- Back up EFS keys and store them securely to avoid losing access to encrypted files.
- Use strong passwords for recovery keys to enhance security.
- Regularly verify access to encrypted files after password changes or key imports.

### Tools Used
- **EFS**: For file encryption on Windows.
- **Command Line**: For user, file, and directory management.
- **PFX Files**: For encryption key recovery.

### Project Resources
- **Project Link**: [Security Lab 20: Encryption EFS](https://github.com/StephVergil/Security-Lab-20-Encryption-EFS/blob/main/Security%20Lab%2020%20Encryption%20EFS.docx.pdf)
- [Microsoft EFS Documentation](https://docs.microsoft.com/en-us/windows/security/information-protection/efs)

### Conclusion
This lab demonstrates the critical role of encryption and secure key management in protecting sensitive data. By leveraging EFS and strong password practices, users can ensure data confidentiality and prevent unauthorized access.

### Disclaimer
This project was conducted in a controlled environment. Unauthorized use of these techniques or tools outside such an environment may violate ethical guidelines and legal regulations.

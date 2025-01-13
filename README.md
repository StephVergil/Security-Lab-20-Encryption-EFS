# Security Lab: Encryption EFS

This lab explores the practical implementation and management of the Encrypting File System (EFS) on Windows systems. By configuring EFS, managing encryption keys, and examining password policies, the lab highlights the role of secure data encryption in protecting sensitive information from unauthorized access.

---

## Objectives
- Understand the file system requirements and commands for EFS functionality.
- Learn to back up and restore EFS encryption keys.
- Explore the impact of password policies on accessing encrypted files.
- Use Personal Information Exchange (PFX) keys for recovering encrypted files.

---

## Key Results

### **File System Requirements**
- **NTFS Required**: EFS operates only on NTFS file systems, which support advanced security features.

### **Creating Users, Files, and Directories**
- **Steps**:
  - **Create a User**: Add a new user account.
    ```bash
    net user jessejames cowboy /add
    ```
  - **Create a File**: Generate a sample file for encryption.
    ```bash
    echo 123-45-6789 > SSN.txt
    ```
  - **Create a Directory**: Organize encrypted files into directories.
    ```bash
    mkdir private
    ```

### **Managing EFS Encryption Keys**
- **Key Backup and Restoration**:
  - Navigate to:
    ```
    START > Control Panel > User Accounts > Manage your File Encryption Certificates
    ```
  - Export encryption keys to a secure location.
- **Password Changes**:
  - **User-Initiated Changes**: Do not affect access to encrypted files.
  - **Administrator-Initiated Changes**: Render encrypted files inaccessible due to new encryption keys.
  - Change password via command:
    ```bash
    net user student 123
    ```

### **Importance of Strong Passwords**
- Protect recovery keys from unauthorized access.
- Enhance overall system security by preventing brute-force attacks on PFX files.

### **Recovering Files Using PFX**
- **Password Requirement**: Mandatory during PFX key installation to ensure secure access.
- **Verification**:
  - Confirm successful certificate import through the Certificate Import Wizard.
  - Open encrypted files to verify access.
- **EFS Indicators**:
  - Encrypted files appear in green text.
  - Imported keys enable file decryption and access restoration.

---

## Recommendations
- **Secure Key Backups**: Regularly back up EFS keys and store them securely to prevent data loss.
- **Strong Password Practices**: Implement complex passwords for recovery keys to enhance security.
- **Regular Testing**: Periodically verify access to encrypted files and functionality of backup keys.
- **Password Policy Enforcement**: Use policies that ensure strong and unique passwords for users.

---

## Tools Used
- **EFS (Encrypting File System)**: Native Windows feature for encrypting data.
- **Command Line**: Used for user, file, and directory management.
- **PFX Files**: Personal Information Exchange format for encryption key recovery.

---

## Project Resources
- **Project Link**: [Security Lab 20: Encryption EFS](https://github.com/StephVergil/Security-Lab-20-Encryption-EFS/blob/main/Security%20Lab%2020%20Encryption%20EFS.docx.pdf)
- [Microsoft EFSRPC Protocol Documentation](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-efsr/08796ba8-01c8-4872-9221-1000ec2eff31) 
- [File Encryption Documentation](https://learn.microsoft.com/en-us/windows/win32/fileio/file-encryption) 

---

## Conclusion
This lab underscores the critical role of encryption in safeguarding sensitive data. By leveraging EFS, managing encryption keys, and enforcing strong password policies, organizations can enhance data confidentiality and mitigate risks of unauthorized access. Regular backups and secure management practices ensure the reliability of EFS in real-world scenarios.

---

## Disclaimer
This project was conducted in a controlled academic environment. Unauthorized use of these techniques or tools outside such an environment may violate ethical guidelines and legal regulations.

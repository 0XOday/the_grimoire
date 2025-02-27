Registry Editor

The Windows registry provides a remotely accessible database for storing operating system, device, and software application configuration information. You can use the **Registry Editor (regedit.exe)** to view or edit the registry.

### Registry Keys

The registry is structured as a set of five root keys that contain computer and user databases. The HKEY_LOCAL_MACHINE (HKLM) database governs system-wide settings. The HKEY_USERS database includes settings that apply to individual user profiles, such as desktop personalization. HKEY_CURRENT_USER is a subset of HKEY_USERS with the settings for logged in user.

![](https://s3.amazonaws.com/wmx-api-production/courses/35011/images/9411-1639515334205-windows_10_21h2_registry_editor_root.png)

Registry root keys. Troubleshooting and editing activity is usually focused on either HKLM or HKCU. (Screenshot courtesy of Microsoft.)

The registry database is stored in binary files called hives. A hive comprises a single file (with no extension), a .LOG file (containing a transaction log), and a .SAV file (a copy of the key as it was at the end of setup). The system hive also has an .ALT backup file. Most of these files are stored in the C:\Windows\System32\Config folder, but the hive file for each user profile (NTUSER.DAT) is stored in the folder holding the user's profile.

### Editing the Registry

Each root key can contain subkeys and data items called value entries. You can use the **Find** tool to search for a key or value.

Subkeys are analogous to folders, and the value entries are analogous to files. A value entry has three parts: the name of the value, the data type of the value (such as string or binary value), and the value itself.

![](https://s3.amazonaws.com/wmx-api-production/courses/35011/images/5518-1639515344299-windows_10_21h2_registry_editor_hklm_run_new_string.png)

Editing the registry. (Screenshot courtesy of Microsoft.)

If you want to copy portions of the registry database and use them on other computers, select **File > Export Registry File**. The file will be exported in a registry-compatible format and can be merged into another computer's registry by double-clicking the file (or calling it from a script).
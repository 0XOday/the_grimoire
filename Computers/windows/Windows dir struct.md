![[typical-windows-directory-structure.png]]
### System Files

System files are the files that are required for the operating system to function. The root directory of a typical Windows installation normally contains the following folders to separate system files from user data files:

- **Windows**—The system root, containing drivers, logs, add-in applications, system and configuration files (notably the System32 subdirectory), fonts, and so on.
- **Program Files\Program Files (x86)**—Subdirectories for installed applications software. In 64-bit versions of Windows, a Program Files (x86) folder is created to store 32-bit applications.
- **Users**—Storage for users' profile settings and data. Each user has a folder named after their user account. This subfolder contains NTUSER.DAT (registry data) plus subfolders for personal data files. The profile folder also contains hidden subfolders used to store application settings and customizations, favorite links, shortcuts, and temporary files

### File Explorer Options

The **File Explorer Options** applet in Control Panel governs how Explorer shows folders and files. On the **General** tab, you can set options for the layout of Explorer windows and switch between the single-click and double-click styles of opening shortcuts.

![](https://s3.amazonaws.com/wmx-api-production/courses/35011/images/4086-1639514621971-windows_10_21h2_file_explorer_options.png)

General and view configuration settings in the File Explorer Options dialog. (Screenshot courtesy of Microsoft.)

On the **View** tab, among many other options, you can configure the following settings:

- **Hide extensions** for known file types—Windows files are identified by a three- or four-character extension following the final period in the file name. The file extension can be used to associate a file type with a software application. Overtyping the file extension (when renaming a file) can make it difficult to open, so extensions are normally hidden from view.
- **Hidden files and folders**—A file or folder can be marked as "Hidden" through its file attributes. Files marked as hidden are not shown by default but can be revealed by setting the "Show hidden files, folders, and drives" option.
- **Hide protected operating system files**—This configures files marked with the System attribute as hidden. It is worth noting that in Windows, File/Resource Protection prevents users (even administrative users) from deleting these files anyway.

### Indexing Options

You can configure file search behavior on the **Search** tab of the File Explorer Options dialog. Search is also governed by settings configured in the **Indexing Options** applet. This allows you to define indexed locations and rebuild the index. Indexed locations can include both folders and email data stores. A corrupted index is a common cause of search problems.

![](https://s3.amazonaws.com/wmx-api-production/courses/35011/images/9692-1639514645622-windows_10_21h2_indexing_options_advanced.png)
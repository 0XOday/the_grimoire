*System Restore* allows you to roll back from system configuration changes. System Restore allows for multiple restore points to be maintained ( some are created automatically ) and to roll back from changes to the whole registry and reverse program installations and updates.

*Configuring System Protection*
Use the **System Protection** tab (Opened via advanced System settings) to select which disk(s)
to enable for system restore and configure how much disk capacity is used. The disk must be formatted with NTFS, have a minimum 300 MB free space, and over 1 GB in size

Restore points are created automatically in response to application and update installs. They are also created periodically by Task scheduler. Windows will try to create one when it detects the PC is idle if no other restore points have been created in the last seven days. You can also create a restore point manually.

*Using System Restore*
To restore the system, open System Restore tool (rstrui.exe) You can also run System Restore by booting from the product disk or selecting Repair You Computer from the recovery environment 

Note : System Restore does not usually reset passwords (that is, passwords will remain as they were before you ran the restore tool), but System Restore does reset passwords to what they were at the time the restore point was created if you run it from the product disk.
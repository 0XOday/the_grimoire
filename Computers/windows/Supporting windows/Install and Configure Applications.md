
In a 64-bit Windows environment, 32-bit application files are installed to the `Program Files (x86)` folder, while 64-bit applications are stored in `Program files` (unless the user chooses custom installation options) Windows 64-bit shared system files (DLLs and EXEs) Are stored in `%SystemRoot%\system32` ; that is, the same folder as 32-bit versions of Windows files for 32-bit versions are stored in `%SystemRoot%\syswow64`

**Distribution methods**

An app distribution method is the means by which the vendor makes it available to install. Many apps are published through app stores, in which case the installation mechanics are handled automatically.
Desktop applications are installed from a setup file. In Windows, These use either .EXE or .MSI extensions. Apps for macOS can use DMG or PKG formats. linux packages use DEB packages with the APT package manager or RPM for YUM

The setup file packs the application's executable(s), configuration files, and media files within it. During setup, the files are extracted and copied to a directory reserved for use for application installation.

This type of setup file can be distributed on physical media, such as CD/DVD or a USB thumb drive, or it could be downloaded from the internet. When downloading an installer from an internet location, it is imperative to verify the authenticity and integrity of the package and to scan it for malware. Windows uses a system of digital signatures to identify valid developers and software sources. Linux software is verified by  publushing hash value of the package. After download you should generate your own hash of the package and compare it to the value published by the package maintainer. 

**Other Considerations**

To maintain a secure and robust computing environment, potentail impacts from deploying new applications must be assessed and mitigated. it is important that the IT department maintains control and oversight of all third-party software installed to network hosts. Unsanctioned software and devices--shadow IT-- raises substantial operational and business risks. 

**Impact to Business**

In a corporate environment, any application that is installed must also be supported. 

* Licensing -- Commercial software must be used within the constraints of its license. this is likely to restrict either the number of devices on which the software can be installed or the number of users that can access it. installing unlicensed software exposes a company to financial and legal penalties. 
* Support - software might be available with paid-for support to obtain updates, monitor and fix security issues, and provide technical assistance. Alternatively security monitoring and user assistance could be performed  by internal staff, but the impact to IT operations still needs assessing 
* Training - complex apps can have a substantial and expensive user-training requirement. This can be ongoing cost as new versions can introduce interface or feature changes that require more training or new employees require initial training. If the app is supported internally, there might also be technical training requirement to ensure staff can provide support and maintain the application is a secure state.

**Impact to Operation**

As well as the broader business impacts, a project to deploy a new application must also consider impacts to operation. Where there are hundreds desktops, The IT department will need to use automated tools to deploy, update, and support the app.

When an organization wants to deploy an application to a number of desktops, it is likely to use a network-based installer. In this scenario, the setup file is simply copied to a shared folder on the network, and the client computers run the setup file from the network folder. In windows, you can use policies-- Group Policy Objects (GPOs) -- to set a computer to remotely install an application from a network folder without any manual intervention from an admin. Products such as centrally managed antivirus suites often support "Push" deployments tools to remotely install the client or security sensor on each desktop. 
One  advantage of using a tool such as GPO to deploy applications is that a user does not have to log on to the local client with admin priv. Writing/modifying permissions over folders to which the application-executable files are installed are restricted to admin level accounts. This prevents unauthorized modification of the computer or the installation of programs that could threaten security policies. The setup file for a deployed application can run using a service account. 

To run an application, the user needs to be granted read/execute permission over the application's installation directory. Any files created using the application or custom settings/preferences specific to a particular user should be saved to the user's home folder/profile than the application directory.

**Impacts to Device and to Network**

When selecting applications for installation on desktops, proper security considerations need to be made regarding potential impacts to the device and to the network. The principal threat is that of a Trojan Horse; 















































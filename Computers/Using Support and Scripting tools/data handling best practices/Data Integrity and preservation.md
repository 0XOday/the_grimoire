### Documentation of Incident and Recovery of Evidence

The general procedure for ensuring data integrity and preservation from the scene of a security incident is as follows:

1. Identify the scope of the incident and the host systems and/or removable drives that are likely to contain evidence. If appropriate, these systems should be isolated from the network.
2. Document the scene of the incident using photographs and ideally video and audio. Investigators must record every action they take in identifying, collecting, and handling evidence.
3. If possible, gather any available evidence from a system that is still powered on, using live forensic tools to capture the contents of cache, system memory, and the file system. If live forensic tools are not available, it might be appropriate to video record evidence from the screen.
4. If appropriate, disable encryption or a screen lock and then power off each device.
5. Use a forensic tool to make image copies of fixed disk(s) and any removable disks. A forensic imaging tool uses a write blocker to ensure that no changes occur to the source disk during the imaging process.
6. Make a cryptographic hash of each source disk and its forensic image. This can be used to prove that the digital evidence collected has not been modified subsequent to its collection.
7. Collect physical devices using tamper-evident bags and a chain-of-custody form, and transport to secure storage.
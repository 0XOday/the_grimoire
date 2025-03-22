* An alternative to file encryption
* BitLocker is FDE (Full disk encryption)
* Full disk encryption also encrypts the swap, print queues, temporary files etc
* Bitlocker to go can be used on removable drives
* Users don't have to remember passwords 
* Bitlocker can use the TPM chip to tie in the drive to that motherboard 
	* The TPM must be configured with an owner password (often the system password set in firmware). You can manage TPM settings from Windows using the TPM Management snap-in (select **_TPM Administration_** from the BitLocker applet).
* a recovery key is generated which should be stored in a safe location 
* Best practice is to sanitize data 
* Use disk erasing/wiping software ensures that old data is destroyed by writing over old data ( linux shred tool or dd dev/urandom to the disk )
* Low level format 
	* vendors supply this tool
	* resets a disk to factory condition 
	* Secure Erase (SE) - preforms zero-filling on HDD and marks blocks as empty on SSD's
	* ssd firmware automatically garbage collects then performs the actual erase of each block over time
	* Instant Secure Erase uses the capabilities of self-encrypting drives (SEDs) as a reliable sanitization method for both HDDs and SSD
* GFS scheme ( Grand father - son ) Oldest to freshest scheme labeled as generations 
	* son tapes has the newest backup while retention period is shortest  
	* Grandfather tapes have the longest  retention and oldest data  
* An implementation is as follows 
	* A full backup is performed on a Friday each week. A tape is marked Father
		* 5 different tapes are used 
	* An incremental backup is made every X minutes to X hours to tape. Marked as son 
	* The five tapes are reused each weak in the same order 
	* A full backup called grandfather is made to tape every month
	* After a year the grandfather tape is overwritten 
* Father tapes can be used for a synthetic backup 
* On site 
	* backups are made on site 
	* open to risks of losing data in a disaster 
	* 
	* 
* Off site 
	* Safe from disaster  
	* can be part of redundancy
	* Could be extremely costly based on the online provider  
* Online and offline backups
	* Online backup media is instantly available to perform a backup 
		* Can be compromised by ransomware 
			* some Ransomware is configured to try to access cloud accounts for offsite backups
	* It is considered good practice to have one offline backup incase of compromise 
* 3-2-1 backup rule
	* This is considered best practice 
	* Three copies of data 
	* Across two media types 
	* one copy offline and off site 
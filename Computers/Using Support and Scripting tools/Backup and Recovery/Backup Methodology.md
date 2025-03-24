* Consider how frequent backup are going to be 
	* How much lost work can be tolerated between backups
* How backups are going to be made 
* Retention is how long a backup is kept on standby 
	* Short term retention is important for version control 
	* Aids in the help of recovering from infection 
		* You have to verify if your backups are free from infection for this to be useful 
	* There is legal requirements that an org has to be compliant with 
* Another consideration is how much storage is available for your SAN , Sever that you are backing up to.
* Back up chains 
	* Three types of backups are available
		* "Full only" A full backup of the target but offers the least complex recovery 
			* Considered to have the lowest time and storage requirement 
		* "Full with incremental" Starts with a full back up while keeping track of new files and modified files
			* considered to be complex 
			* has the lowest time and storage req
		* "Full with differential" Starts with a full backup then starts running differential jobs that select new files and modified 
			* Middle of the road approach. Slightly less in complexity than the incremental back up 
* Synthetic backup
	* A backup option for creating full backups with lower data transfer req
	* Not generated directly from the og data built from other backup jobs 
		* backup software makes one more incremental backup
		* 






| Type         | Data                                                             | Backup job time and storage Req | Complexity for recovery  | Archive Attribute |
| ------------ | ---------------------------------------------------------------- | ------------------------------- | ------------------------ | ----------------- |
| Full         | All selected data regardless of when it was previously backed up | High                            | Low                      | cleared           |
| incremental  | New files and files modified since last backup job               | low                             | High (more than one job) | Cleared           |
| Differential | New files and files modified since last full backup job          | Moderate                        | moderate                 | Not Cleared       |

Linux does not have an "official" backup tool. You could create a custom backup soultion using the cron task scheduler and file copy scripts Backup could also use compression utilities, such as tar or gzip. There are plenty of commercial and open source back up products for Linux, however. Some examples include Amanda, bacula, fwbackups and Rsync.

if you want to run a batch of commands or a script to perform a backup or other maintenance tasks, there is a scheduling service called cron. Every user of the system is allowed to schedule programs or tasks in their own personal crontab (cron table). These tables are merged by cron to create an overall system schedule. Every minute, the cron service checks the schedule and executes the programs for that period.

* To add or delete a scheduled job, use the crontab editor. To review a user's crontab jobs, enter the command 
* `crontab -l`
* To remove jobs from the scheduled list, use the command
* `crontab -r`
* To enter the editor, run the command `crontab -e` crontab uses the vi editor by default.

The basic syntax for scheduling a job using crontab includes the following:
* mm - specifies the minutes past the hour when the task is to initiate
* hh - specifies the hour (0-23)
* dd - can be used to specify the date within the month (0-31)
* MM - specifies the month 
* weekday - sets the day of the week 
* command - the command or script to run. 
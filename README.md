Is script is much simpler than all the otehr script I found: It creates a FULL backup, upon which all subsequent incrementals are based. (so: no incremental based on another incremental)
You can run the script daily, many times a day, and it will continue to create (overwriting the existing) an incremental for that day.
When the date changes, the last incremenatl will remain, and a new one will be created, until the day arrives that a new full has to be created.
That day, the backup location will be completely erased, and everyting will start again.

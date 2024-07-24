Is script is much simpler than all the other (beautiful) scripts I found: My script simply creates a FULL backup, upon which all subsequent incrementals are based. (so: no incrementals based on other incrementals)

You can run the script daily, but also many times a day. It will continue to create (overwriting the existing) an incremental for each new run.

When the date changes, the last incremental will remain, and a new incremental will be created, based on the same FULL backup. This continues until the day arrives that a new full has to be created.

That day, the backup location will be completely erased, and everyting will start again.
You can either define that day through a command line option (1-7) or it will be generated based on the numbers in a hostname, and otherwise it will be random, based on $RANDOM. Any day is fine, really.
So you don't HAVE to configure a full day.

It uses ionice to keep a low profile, and generates a little bit of statistics in a file in the target directory. Surprisingly, a INCR backup doesn't run that much faster than a FULL, but their sizes *are* different.

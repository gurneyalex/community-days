============================================
Disaster Recovery with Barman (PostgreSQL)
============================================
Gabriele Bartolini


2ndquadrant italy

Disaster Recovery planning is a valuable investment. 

Business continuity => High availability + disaster recovery

D.R. protects from unintentional errors

Requirements: 

* automated backups
* notifications
* define frequency of backups
* retention policy
* data protection
* availability for recovery

Type of backup: 

* full backup
* incremental backup (the things which changed in the database since the last backup)
* differential backup (log of changes happening)
* hot backup (i.e. without stopping activity)
* logical backup (pg_dump)
* physical backup (copy the files) <- barman

What we want to do: 
hot full differential and incremental
archival and compression... 

Barman

python
gpl3


can ship WAL archives from PG server to Barman backup server and manager
periodical full backups and differential backups

simple CLI

-> barman backup SERVER_ID
-> barman recover SERVER_ID BACKUP_ID

+ optional parameters

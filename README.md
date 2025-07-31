# DATABASE-BACKUP-AND-RECOVERY

*COMPANY*: CODTECH IT SOLUTIONS

*NAME*: BHUMIKA S

*INTERN ID*: CT04DF1481

*DOMAIN*: SQL

*DURATION*: 4 WEEKS

*MENTOR*: NEELA SANTOSH

#In Task 4 of the CODTECH internship, I focused on demonstrating how to back up and restore a MySQL database using command-line tools. The purpose of this task was to show that I can preserve and recover data in case of system failure or accidental deletion. This is a critical part of database administration and something every organization needs to have in place. The task involved both technical steps and an understanding of how real-world systems are protected through backup strategies.

The main tools used in this task were MySQL Workbench and the Windows Command Prompt. MySQL Workbench was used to manage and view the database, run SQL queries, and simulate failure by dropping the database. For the actual backup and restore, I used the command-line tools that come with MySQL specifically mysqldump for backup and mysql for restore. The command-line interface is important because it allows full control over database operations and is used in real production environments, including automation scripts.

I wrote and tested SQL queries in the MySQL Workbench SQL Editor. It’s user-friendly and shows tables, schemas, and results clearly. But for backup and recovery, I needed to switch to the command prompt because that’s where you can run mysqldump and mysql commands. I also used File Explorer to create a custom folder for storing the backup safely, called mysql_backup.

The process started by opening the command prompt and navigating to the MySQL bin directory, which is usually located in C:\Program Files\MySQL\MySQL Server 8.0\bin. This folder contains the tools needed to perform the backup. I created a backup using the following command:

swift
Copy
Edit
mysqldump -u root -p task2_analysis > "C:\Users\Bhumika S\mysql_backup\task2_backup.sql"
This created a complete .sql file containing the structure and data of my database task2_analysis. To simulate a real failure scenario, I opened MySQL Workbench and dropped the database manually. Then I went back to the command prompt, logged into the MySQL shell, and recreated the database using:

pgsql
Copy
Edit
CREATE DATABASE task2_analysis;
Once the new empty database was ready, I restored the backup using the following command:

swift
Copy
Edit
mysql -u root -p task2_analysis < "C:\Users\Bhumika S\mysql_backup\task2_backup.sql"
After running this command, I reopened MySQL Workbench and confirmed that the database had been fully restored with all tables and data exactly as it was before deletion. This showed that the process worked correctly from end to end.

This backup and recovery process is highly applicable in the real world. For example, banks, hospitals, government offices, online stores, and even schools all rely on regular backups to protect data. If a crash happens or someone accidentally deletes something, being able to restore from a recent backup is what prevents disaster. Large companies automate this process daily or hourly using scripts that run similar commands.

What I learned from this task is not just how to run the commands, but also how important it is to handle paths properly, give correct permissions, and verify each step. I encountered common issues like “Access Denied” and “Path Not Found” and fixed them by creating a proper folder and using quotes around paths that had spaces. I also learned how important it is to test the recovery process not just assume that a backup will work.

Overall, Task 4 made me confident in managing MySQL backups using both Workbench and the command line. I now understand how to back up data in .sql format, how to restore it completely, and how to organize it all clearly for submission or real-life usage. This task showed me how critical backups are, and gave me hands-on practice with something every professional database developer should know.










# HDFS Operations Guide

This guide provides a structured set of commands for performing various operations in HDFS.

## 1. Create a Directory in HDFS

```bash
hadoop fs -mkdir /lab1
Description: Creates a new directory named lab1 in HDFS.

2. Copy the purchases.txt File into HDFS

hadoop fs -put purchases.txt /lab1/
Description: Copies the local file purchases.txt into the lab1 directory in HDFS.

3. Display the Contents of the lab1 Directory

hadoop fs -ls /lab1
Description: Lists the contents of the lab1 directory.

Replication Factor To check the replication factor of the file:

hadoop fs -stat %r /lab1/purchases.txt
Description: Returns the replication factor for purchases.txt.

4. Identify the Size of the purchases.txt File
bash
Copier le code
hadoop fs -du -h /lab1/purchases.txt
Description: Displays the size of the purchases.txt file in a human-readable format.

5. Identify the Number of Blocks Related to the File purchases.txt
bash
Copier le code
hadoop fs -stat %b /lab1/purchases.txt
Description: Returns the number of blocks used by the purchases.txt file.

6. Display the First 25 Lines of the File purchases.txt

hadoop fs -cat /lab1/purchases.txt | head -n 25
Description: Displays the first 25 lines of the purchases.txt file.

7. Copy the File purchases.txt into purchases_hdfsCopy.txt

hadoop fs -cp /lab1/purchases.txt /lab1/purchases_hdfsCopy.txt
Description: Creates a copy of purchases.txt as purchases_hdfsCopy.txt in HDFS.

8. Copy the File purchases.txt into purchases_copy.txt in the Local File System

hadoop fs -get /lab1/purchases.txt /path/to/local/directory/purchases_copy.txt
Description: Copies purchases.txt from HDFS to the specified local directory as purchases_copy.txt. Replace /path/to/local/directory/ with the actual path.

9. Check the Entire File System for Inconsistencies or Issues

hadoop fsck /
Description: Checks the entire HDFS for inconsistencies and reports any issues.

10. Delete the File purchases.txt from HDFS

hadoop fs -rm /lab1/purchases.txt
Description: Deletes the purchases.txt file from the lab1 directory in HDFS.

11. Delete the Directory lab1 from HDFS

hadoop fs -rmdir /lab1
Description: Removes the lab1 directory from HDFS. Ensure the directory is empty before deletion.





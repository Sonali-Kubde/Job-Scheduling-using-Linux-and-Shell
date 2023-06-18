# Job-Scheduling-using-Linux-and-Shell

The code does the following job
Download the following zip file with the wget command:
1 Download the file through cmd
wget https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-LX0117EN-SkillsNetwork/labs/Final%20Project/important-documents.zip


2 Unzip the archive file:
unzip -DDo important-documents.zip

(-DDo to overwrite and not restore original modified date)



3. Update the file’s last modified date to now:
touch important-documents/*


4. Test script using the following command:
./backup.sh important-documents .

This should have created a file called backup-[CURRENT_TIMESTAMP].tar.gz in your current directory
![image](https://github.com/Sonali-Kubde/Job-Scheduling-using-Linux-and-Shell/assets/81162473/057e867c-076e-4599-a8f5-76630811a38d)

Test the cronjob to see if the backup script is getting triggered by scheduling it for every 1 minute.
*/1 * * * * /usr/local/bin/backup.sh /home/project/important-documents /home/project


# HTI-Storage-Server
This a simple walkthrough to our project, with steps on how to get it installed and running.
The project was done on both Windows OS, and Linux OS, so better to setup a virtual Box for Linux


Installing Kali Linux

Virtual-Box Download link (106MB): https://download.virtualbox.org/virtualbox/7.0.12/VirtualBox-7.0.12-159484-Win.exe
Kali Linux Pre-built Virtual Machine (3.1GB): https://cdimage.kali.org/kali-2023.4/kali-linux-2023.4-virtualbox-amd64.7z
Follow this video: https://youtu.be/iu-puVuUuzU?t=120



OPTIONAL
Installing Windows VM
If you want to create a virtual windows machine just for the project, 
you can do that by following this video: https://www.youtube.com/watch?v=sBzL_zoYt6o



Project Installation

1- Download "Project Files.rar", and extract it on desktop. "should look like this https://i.imgur.com/TXzu9tg.png"
2- Download both Xampp and snort and install them to default directories. "download links in the .txt files"
3- Extract "filehosting Database" in desktop. "Should look like tHis https://i.imgur.com/c6b4Vsv.png"4
4- After installing Xampp, open it, launch both Mysql + Apache servers, and click on the "Shell" icon on the right side
5- in the shell type the next code:
            ```
            mysql -u root -p
            ```
            you will be asked to enter a password, just press enter, you will enter the Mysql databse, enter the next code to create a Database:
            ```
            create Database filehosting;
            ```
            Verify that you have successfully created a database with this command
            ```
            show databases;
            ```
            should look like this "https://i.imgur.com/qQY9R8l.png"
            Finally, exit our of the Mysql by typing
            ```
            exit
            ```
            back in the main Shell command prompt, type the next command
            ```
            cd %userprofile%\Desktop
            mysql -u root -p filehosting < filehosting.sql
            ```
            this should import the pre built database, to the database you just created.



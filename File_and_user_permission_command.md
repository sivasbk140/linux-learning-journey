🔐 CHANGING PERMISSIONS FOR THE USER

➡️ Remove read permission: `chmod u-r filename.txt` 🚫📄  
➡️ Add full permissions: `chmod u+rwx filename.txt` ✅🛠️

***************************************************************************************************************

👤 CREATE NEW USER

➡️ Use `sudo useradd newusername -m` 🧑‍💻  
(Makes a home directory for the new user 🏠)

🔐 Set password: `sudo passwd newusername` 🔒🔑  
✳️ Enable Bash shell: `sudo usermod -s /bin/bash newusername` 🖥️  
🔚 Exit current user: `exit` 🚪

*******************************************************************************************************************

👥 CREATING GROUPS

➡️ Create a new group: `sudo groupadd NEWGROUPNAME` 🆕👥  
Helps set shared permissions for users in the group 🎯🔐

*******************************************************************************************************************

👤➡️👥 ADD USER TO GROUP

➡️ Add user to group: `sudo usermod -aG NEWGROUPNAME newusername` 🔗👤👥

*****************************************************************************************************************************

👀 CHECK USER’S GROUP MEMBERSHIP

➡️ See groups a user belongs to: `groups newusername` 🧑‍💻🔍

****************************************************************************************************************************

🧑‍🤝‍🧑 ALLOW FILE PERMISSION TO OTHER USERS

➡️ Grant access: `sudo chmod o+rx /home/username`  
🔤 `o` stands for “others” — gives read and execute rights 👀📂

*********************************************************************************************************************************

🧑‍🤝‍🧑 FILE PERMISSIONS TO GROUPS

📌 Step 1: Change file ownership to group  
➡️ `sudo chown :newgroupname filename` 👥📁

📌 Step 2: Remove group permissions  
➡️ `sudo chmod g-rwx filename.txt` ❌🔐  
Prevents users in that group from accessing the file

********************************************************************************************************************************

🔁 CHANGING FILE OWNERSHIP

➡️ Change owner to another user: `sudo chown desiredusername filename.txt` 👤📄  
➡️ Change owner to a group: `sudo chown :desiredgroupname filename.txt` 👥📄

**************************************************************************************************************************************

📦 COMPRESSING & EXTRACTING FILES

🧵 Using **tar**:

➡️ Compress:  
`tar czvf archive-name.tar.gz source-file/` 📦📝

➡️ Extract:  
`tar xzvf archive-name.tar.gz -C ~/target_directory/` 🗃️📂

🧵 Using **zip**:

➡️ Compress:  
`zip -r archive.zip source-folder/` 📦🔐

➡️ Extract:  
`unzip archive.zip -d ~/target_directory/` 📂🎯

🧵 Using **gzip**:

➡️ Compress directly:  
`gzip folder/filename.txt` 🧮📑

➡️ Extract (decompress):  
`gunzip filename.txt.gz` 📂🧹

***********************************************************************************************************************************

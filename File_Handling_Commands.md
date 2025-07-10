🔗 LINKS

It has two types:
1️⃣ Symbolic Links  
2️⃣ Hard Links

***********************************************************************************************

🔗 SYMBOLIC LINK (-s)  
➡️ Only stores the address or path of the original file. It points directly to that physical file.  

🧾 SYNTAX:  
ln -s ~/relative/path/filename ~/relative/path/desired-link-name  

⚠️ NOTE:  
If the source file is deleted, the virtual (symbolic) link breaks.  
To force relinking, use:  
ln -sf ~/source-file-path ~/virtual-file-path  

💡 (sf) means “symbolic force” — it forces the link to reestablish with another file.

***********************************************************************************************

🧬 HARD LINK  
➡️ Contains exact data from the original file.  
Has same inode number and shares memory between original and linked file.  

📄 SYNTAX:  
ln ~/path/to/original-file ~/path/to/hard-link-name  

🧠 NOTE:  
Deleting the original symbolic link affects its virtual reference.  
But with hard links, deletion of original won’t break the linked copy — because it references the inode directly 🧩📁

***********************************************************************************************************

✏️ RENAMING FILES (mv)  
➡️ Rename files with:  
mv ~/Documents/filename ~/Documents/new-filename 📂🔄

***********************************************************************************************************

🗑️ DELETING FILES AND DIRECTORIES (rm)  
➡️ Removes files or folders using:  
rm ~/directory/filename  

🧠 NOTES:  
You can delete multiple files in one go just like creating multiple ones.  

💬 Interactive deletion:  
`rm -i ~/folder/file` → Prompts “Are you sure?” ✅❌  

🧹 Recursive deletion:  
`rm -r ~/folder/` → Deletes the folder and all files inside  

🚫 You can’t delete folders unless files inside are removed first.

***************************************************************************************************************

👀 COMMANDS FOR VIEWING FILES

📖 cat → Shows all content inside a file  
🔝 head → Displays first 10 lines  
📜 SYNTAX: head -n 10 ~/folder/filename  

🔚 tail → Displays last 10 lines  
📜 SYNTAX: tail -n 10 ~/folder/filename  

🧭 more → Shows content page-by-page (screen-adaptive)  
📜 SYNTAX: more ~/folder/filename  

📝 vi / vim → Edits and views content in interactive mode  
⌨️ Exit with: shift + colon → type `q`

************************************************************************************************************************

🔍 FINDING FILES IN LINUX

🔎 find  
1️⃣ Finds files and their paths  
📜 SYNTAX: find /path/from/home/ -name "filename.txt"

2️⃣ Find directories only  
📜 SYNTAX: find /absolute/path/ -type d  

3️⃣ Find files only  
📜 SYNTAX: find /absolute/path/ -type f  

4️⃣ Find files modified in last 7 days  
📜 SYNTAX: find /absolute/path/ -mtime -7

🚀 locate  
Fast file search using a database  
📜 SYNTAX: locate "filename.txt"

🧩 which  
Tells where command binaries are stored  
📜 SYNTAX: which ls  
📜 SYNTAX: which cat

📂 whereis  
Shows location of command source, binary, and help docs  
📜 SYNTAX: whereis ls

*******************************************************************************************************************

🧠 FINDING FILES WITH GREP

🕵️‍♂️ find with grep → Find files containing specific text or keywords  

📜 SYNTAX:  
find ~/directory/ -type f -exec grep -l "keywords" {} \;

***********************************************************************************************************************

🧵 FILE EDITORS

📝 nano → Creates or edits a file instantly  
📜 SYNTAX: nano ~/folder/filename.txt  
💾 Save: Ctrl + O  
❌ Exit: Ctrl + X  

🎨 vim → Advanced file editing  
📜 SYNTAX: vim ~/folder/filename.extension  
🛠️ Press `i` to start editing  
💾 Save & quit: esc → shift + : → type `wq`

***********************************************************************************************************************************

🔐 FILE PERMISSIONS

R → Read 📖  
W → Write ✏️  
X → Execute ⚙️  

📄 - → File  
📁 d → Directory  
🔗 l → Link

📊 Permission breakdown:
- rw- for user  
- r-- for group  
- r-- for others

***********************************************************************************************

#### Find Files Using Name in Current Directory
` find . -name script.txt`

#### Find Files Under Home Directory
` find /home -name script.txt`

#### Find Files Using Name and Ignoring Case
` find /home -iname script.txt `
./script.txt
./Script.txt

#### Find Directories Using Name
` find / -type d -name Script `

/Script

#### Find PHP Files Using Name
` find . -type f -name script.php `
./script.php

#### Find all PHP Files in the Directory
` find . -type -f "*.php" `

./script.php
./nir.php
./manj.php

#### Find Files With 777 Permissions
` find . -type -f -perm 0777 -print `

#### Find Files Without 777 Permissions
` find . -type f ! -perm 0777 `

#### Find SGID Files with 644 Permissions
` find / -perm 2644 `

#### Find Sticky Bit Files with 551 Permissions
` find . -perm 1551 `

#### Find SUID Files
` find / -perm /u=s ` 

#### Find Read-Only Files
` find / -perm /u=r `

#### Find Executable Files
` find / -perm /a=x `

####  Find Files with 777 Permissions and Chmod to 644
` find / -type -f -perm 0777 - print - exec chmod 644 {} \; `

#### Find Directories with 777 Permissions and Chmod to 755
` find / -type d -perm 0777 -print -exec chmod 755 {} \; `

#### Find and remove single File
` find . -type f -name "Script.txt" -exec rm -f {} \; `

#### Find and remove Multiple File
` find . -type f -name "*.txt" -exec rm -f {} \; `

#### find all empty files
` find /tmp -type f -empty `

#### Find all Empty Directories
` find /tmp -type d -empty `

####  File all Hidden Files
` find /tmp -type f -name ".*" ` 

#### Find Single File Based on User
` find / -user manoj -name script.txt `

#### Find all Files Based on Group
` find /home -group devloper `

#### Find Particular Files of User
 ` find /home -user manoj -iname "*.txt" `
 
####  Find Last 50 Days Modified Files
` find / -mtime 50 `
 
#### Find Last 50 Days Accessed Files
 ` find / -atime 50 `
 
#### Find Last 50-100 Days Modified Files
 ` find / -mtime +50 -mtime -100 `
  
#### Find Changed Files in Last 1 Hour
 
` find / -cmin -60 `
 
 ##### Find Modified Files in Last 1 Hour
 ` find / -min -60 `

#### Find Accessed Files in Last 1 Hour
` find / -amin -60 `

####  Find 50MB Files
` find / -size 50M `

### Find Size between 50MB – 100MB
` find / -size +50M -size -100M `

## Find and Delete 100MB Files
` find / -type f -size +100M -exec rm -f {} \; `

## Find all .mp3 files with more than 10MB and delete them using one single command.
 `find / -type f -name "*.mp3" -size +10M -exec rm {} \; `

# Demostration-of-access-control,-Symmentric-encryption and decryption
Question:
You are the security admin for ABC lnc. and you have been tasked with creating accounts for the five (5) new employees. Two of the employees will belong to the Finance dept., Two other will belong to Marketing dept., while the last employee will not be a member of any depts.
There is a confidential file name "account.txt" which requires all but members of Finance dept. to have read and write (RW) access to the file and members of Marketing dept. only have read (R) access to the file.
Finally, ensure that this file is encrypted with the appropriate encryptionopens type

Steps to the Solution of the task:
i. Create the content of the file, file name and encrypt it at once using symmentric encryption using Kali linux with command line: echo This passkey to the main vault is "KL03678sh" | openssl aes-256-cbc-pbkdf2 -a -salt -out account.txt -k mypassword           Note: the file account.txt has been created and encrpted to view use "cat acount.txt"
ii. Create the dept by using "sudo addgroup Finance and sudo addgroup Marketing" 
iii. To add new employees to existing dept. use sudo useradd -g finance jay and repeat same for kay, also use sudo useradd -g marketing ganny and repeat same for danny
iv. create access to the last employee with dept. sudo useradd john
v. to grant access to finance and marketing dept. use setfacl -m g:finance:rw account.txt and setfacl -m g:marketing:r account.txt
to view what you have done getfacl account.txt

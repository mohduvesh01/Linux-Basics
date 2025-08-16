# 🔐 6. File Permissions
Symbol	Meaning
r     	Read
w     	Write
x     	Execute


# Permission-Example:
-rwxr-xr--
Owner: read, write, execute
Group: read, execute
Others: read

# Command-Description

chmod 755 file.sh	Change permissions using numeric mode
chmod +x script.sh	Make script executable
chown user:group file	Change file ownership

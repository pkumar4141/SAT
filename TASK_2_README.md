we have a file descriptor limit when the iimit exceeds we face this kind of error

ulimt -a |grep open 

will give the open files 

we can change the limit by 

sysctl -w fs.file-max=500000 in order to make the permanent even after reboot use update fs.file-max in  /etc/sysctl.conf
sysctl -p applies the chnage immedaitely



vi /etc/security/limits.conf for user level limits
for process specific 

/proc/pid/limit to check file descriptor for specific process


we have a file descriptor limit, when the iimit exceeds we face this kind of errors.

Below are the steps to resolve the issue

`ulimt -a | grep open` if command doesn't work, try `ulimit -n`

above command will give the file descriptor limit 

we can change the limit by 

`sysctl -w fs.file-max=500000` in order to make the permanent even after reboot use update fs.file-max in  /etc/sysctl.conf
`sysctl -p` applies the chnage immedaitely



`vi /etc/security/limits.conf` for user level limits
for process specific 

`/proc/pid/limit` to check file descriptor for specific process


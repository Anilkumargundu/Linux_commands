Basic commands in Linux
lsb_release -a  ###to check the version of ubuntu
df -h    ##check the space
du -h /folder_name   ## check space of specific folder
du -sh *  ##to check the memory consumed by each folder (used mostly by me)
apt list --installed ## to check the list of installed applications
chmod 775 folder_name    ### to provide read, write and other permissions when the file creates
visudo           ##to add sudo usser for admin access""
cat /etc/passwd      ####path that shows the user app_name
cat /etc/shadow             ###########to know the shell and home folder

cat   ## to see the content int the file
cat auth.log | less   ##(to see page by page)
grep 'keyword" (to seach a specific word in the file)
cat file_name | grep 'search_word"
adduser User_name (to add a account)
sudo apt install app_name
sudo apt update
ls -a   ## to see the hidden files
find ~ -name "*your_filename*"  ### this will search for the fine_name in all paths

git checkout -b branch_name
###access the ubuntu from windos (WSL install)
Windos + E and \\wsl$ to access linux

## access windows from ubuntu 
/mnt


#####lock file
#find . -name '*lck*' '*panic.log*'
#find . -name '*lck*' '*panic.log*' -exec rm {} +
find . \( -name '*lck*' -o -name '*panic.log*' \)
find . \( -name '*lck*' -o -name '*panic.log*' \) -exec rm {} +








ANALOG - OP-AMP 
Virtual short is valid until which point - Virtual short of the op-amp is valid until the output of the op-amp saturates (It doesnt follow the virtual ground once the output of the opamp saturates)
The virtual short condition is valid as long as the op-amp operates within its linear region. When the op-amp's output reaches its saturation point (i.e., it can no longer increase or decrease its output voltage), the virtual short condition no longer holds. In essence, the virtual short is dependent on the op-amp's ability to adjust its output to maintain the near-zero voltage difference between its inputs. Once it saturates, it loses this ability

Miller capacitance :
Any impedance connected connected between two nodes (say p and q) in a circuit can always be resolved into two impedences : one between p and GND, other between q and GND as long as there is a stringant relation between p and q at low frequences irrespective of the presence of the impedance between p and q. This means even though the impedance between p and q is absent, the relation between p and q still exists
Any impedance connected between two nodes (say p and q) in a circuit can always be resolved into two impedances: one between p and GND, and the other between q and GND, provided there is a strong relationship between the voltages at p and q at low frequencies, regardless of the presence of a direct impedance between p and q. This implies that even if the direct impedance between p and q is absent, the relationship between their voltages still exists.

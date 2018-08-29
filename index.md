remoting from school:

remote in through putty - port 22 - connection type ssh
host name: bshevela@imagine.mines.edu
save session through putty - name session
transfer files through cmd prompt - pscp bshevela@imagine.mines.edu:/u/af/ao/bshevela
pwd = present working directory

remoting from home:

same process with putty downloaded and signed into mines BPM

man command - looks into linux documentation
man argument(some other command)
man -k sort looks for sort in manual
in general: command (command line options)arguments and whatever
date = date and time -u = utc time
date "+Today's date: %d. The time is %t"

CheatCheet.lnx

Creating a script

script -a --timing=week-2.tm week-2.out
-a =  append
exit - exits script
scriptreplay --timing week-2.tm week-2.out

who - all users signed into server
whoami - userID
(pts/whatever) - terminal
tty is your terminal

echo whatever echos whatever

bc - opens calculator
scale=2 - changes decimal
ibase=2 - changes base up to 16, 10, 2, 8
ctrl-d exits

home directory -every user has one
working/current directory - where you are currently pwd
parent directory - directory above the working directory
root directory - has no parent

~ stands for home directory
cd ~ changes current directory to home
. stands for current directory
.. parent directory
linux uses tab completion

mkdir arg - creats a directory
rmdir arg - removes directory if empty
rm -r arg - removes everything

ls directory - returns what's in directory
mv filename newname - renames file
mv filename path - moves file
cp filepath new path - copies file

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

tar -xvf filename - uncompresses file  
*  - everything  
file * gives filetype of everything in directory  
file a* - any file that starts with an a  
wget - downloads file  
ls -a - shows hidden files  
? - exactly one character  
file ? - file of length one  

*[ie] - file that ends in i or e*  
file [1-5] - file names 1-5  
[a-cx-z]   - file names a-c x-z  
[!a]*  - file names that don't start with a   

echo {aa,bb,cc} - prints aa bb cc  
echo {0..10} or {z..a}  
echo b{0..3} prints b0-b3  
rm long/path/ {foo, bar} - deletes foo and bar  
touch {a..b}{0..3}{x..z}.txt  -creates a bunch empty files  

NAME="Brandon"  
echo $NAME     - prints name  
echo ${NAME}   - prints name  
echo ${NAME:3} - substring beginning at 3 from name (negtives start from the end)  
echo "My name is ${NAME}s"  

"" - can use variable expansion ${}  
\  - cancels out special meaning  
'' - prints out every character as is  
ls "a*" 'a*' a\* - returns the a* file  

bash shell -desert.sh - running a script  
vim shell-desert.sh  
mkdir -p Dessert/Cobbler - creates files  

echo "Cherry" >> Desert/Cobbler/Filling -redirects cherry to file appending  
echo "The Dessert directory looks like this:"  
ls -R Dessert - lists everything recursivly  
 
echo "Whats your fav?"  
read COBBLER  - gets input from user  

echo $COBBLER >> Dessert/Cobbler/Filling   
echo "The cobbler filling is:"  
cat Dessert/Cobbletr/Filling  
bash -e shell-dessert.sh - exits before error   
bash -x shell-dessert.sh - debugs  


Vim and class things

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

bash shell-desert.sh - running a script  
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

ctrl-l - clears
alt-d  - deletes a word
ctrl-k - copy
ctrl-r - finds in history
ctrl-p - goes through history
!!     - runs last command
Control Signals
bach shell-dessert.sh
ctrl-c - signal interrupt, terminates program
bash -x whatevs shows commands in script
ctrl-d - send endoffile to program, will also exit shell
ctrl-z - sends suspend to program, shows which program was suspended
     works with vim as well
jobs - shows all background jobs
fg commandname - brings back to commandname

Exit Status
0 - command exitted correctly
[1-255]  - command encountered error
echo $? - lists exit status of last run command
   some man files contain exit status
127 - not-found error code
126 - permission error code
130 - ctrl-c terminated prog
1   - general error

Cmd Line Args
bash args.sh returns error no args
bash args.sh some args - correctly executes

vim args.sh
echo "I received $# args" -$# num of args from cmd line
echo "Args list: $@" -$@ entire list of args
echo "First: $1"
echo "second: $2"
echo 
echo "Arg 0 is $0 (this is not counted in " '$# and $0)'

echo 'Hello world' > $1
echo 'Apples' > $2.txt
ls -l some  - shows location of file

while-do-done loop

vim tlw.sh
PROMPT="Enter three little words:"
echo -n "$[PROMPT]"

while read A B C ; do 
        echo Fisrt $[A]
        echo Second $[B]
        echo Third $[C]
        LAST="$[C]"
        echo
        echo -n "$[PROMPT]"
 done
 echo "Your last word was $[LAST]"
 
 exitting with ctrl-d shows last line ctrl-c doesn't
 
ls -l || wc -l -counts number of objects in current directory
grep - searches file/oject for keyword/pattern and outputs them to cmd line
grep --color 'editor' file - keyword highlighted in output
grep -c 'editor' file - prints number of lines with keyword
grep -v - searches for lines that don't contain the keyword
grep -i 'cobbler' file1 file 2 - case insensitive search of multiple files
cat file | grep 'editor' 
ps - lists all current processes
ps | grep 'vim' - searches for and returns vim processes
head -c numLines file - returns first few lines at the top of file
tail -c numLines file - opposite of head
sort file - sorts file and outputs
sort -r - does a random shuffle of file
sort file | tee file - puts sorted file back in file and outputs
ls | tee file - returns output and creates file with ls inside
sort file | uniq -filters out duplicates
sort file | uniq -c - counts number of instances for each word
cat file | tr "[a-z]" "[A-Z]" - turns capitalized version of file
cat file | tr "[:lower:]" "[:upper:]" - turns capitalized version of file
echo "String 1647" | tr -d "[:digits:]" - returns String 
echo "String 1647" | tr -cd "[:digits:]" - returns 1647
cut -c 1,2,3 file - returns first three characters of each line in file
cut -b1-3,5-8 file - returns first three bytes and 5-8
cut -d ',' -f 1,3 file - returns first and third field of file cutting at the commas



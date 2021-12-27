EXERCISE-1:

GETTING STARTED WITH LINUX BASIC COMMANDS AND DIRECTORY STRUCTURE,EXECUTE FILE,DIRECTORY OPERATIONS

OPERATONS:
---------
1)pwd:Present working directory the PWD command is used to find out the content or present working directory.

SYNTAX:$pwd
example:$pwd
o/p:/home/pscmr
..............................................................................................................
2)mkdir:Making the directory the mkdir command is used to make one more new directories.

SYNTAX:$mkdir
example:$mkdir 333
$cd 333
$pwd
o/p:/home/pscmr/333
.............................................................................................................
3)cd:Changing the directory the present directory is it could be change to onther name by using  the cd command .As the user logs in he/she can get into any 
required directory with the help of the cd command

SYNTAX:$cd_file name
example:$mkdir a1
        $cd a1
        $pwd
o/p:/home/pscmr/a1
................................................................................................................
4)cat:concatenate files and print on the standard output
SYNTAX:cat[option]__[filename]__
CREATE A FILE SYNTAX:cat > file name
example:$cat>ex1
hello
hai
welcome to foss lab
[+ctrl Z]
for o/p:$cat ex1
hello
hai
welcome to foss lab 
...................................................................................................................
5)copy:copying the file into onther file
SYNTAX:cp__file1/directory1__file2/directory2
exmaple:$cp ex1 ex2
        $cat ex2
o/p:hello
    hai
    welcome to foss lab
...................................................................................................................
6)rm:remove the file/remove the directory
SYNTAX:rm_file name/directory name
example:$rm c1
        $cat c1
o/p:no such file are in.
.....................................................................................................................
7)head:It is a comman for print first 10 lines in a file.or it print top n number of lines when n is given.
SYNTAX:$head__filename and $head__-n__file name
example:$head ex2
o/p:1
2
3
4
5
6
7
8
9
10
.......................................................................................................................
8)tail:Tail is for last 10 line If n is given it print bottom n number of lines.
SYNTAX:$tail_file name and $tail_-n_file name
example:$tail ex3
o/p:11
12
13
14
15
16
17
18
19
20
............................................................................................................................
9)man:man is a command providing the complete details osf all unix commands in a book.
SYNTAX:$man_ls
       $man_cp
       $man_rm
example:$man ls 
o/p:
ls(1)        -list directory contents
.............................................................................................................................
10)wc:word command
      the command can be used to get count down the total no.of lines,characters contained in the files
SYNTAX:wc_file name
       wc_-l_file name(only for lines)
       wc_-w_file name(only for words)
       wc_-c_file name (only for characters)
example:wc p1
o/p:3 3 15 p1
.................................................................................................................................
11)who:who is shows who is logged on in our systems.
SYNTAX:who_file name
example:$who_b
o/p:system bool  2019-06-10 15:01
to know the no.of users enter into the system
SYNTAX:who_-q_file name
       who_|wc_-l_file name
example:$who_-q_b
o/p:1
//////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
EXPERIMENT-3
AIM:Shell programming :write shell script to show various system configuration like 
1.currently logged user and his logname
2.your current shell
3.your home directory
4.your operating systemtype
5.your current path setting
6.your current working directory
7.show currently logged number of users
SOURCE CODE:
echo"1.currently logged user and his logname\n2.your current shell\n3.your home directory\n4.your operating systemtype\n5.your current path setting\n
6.your current working directory\n7.show currently logged number of users"
echo"enter option"
read op
case $op in
1)echo "currently logged user $USER and his log name is $LOGNAME"
;;
2)echo "current shell is $SHELL"
;;
3)echo "home directory is $HOME"
;;
4)echo "current operating system type proc/version"
;;
5)echo "your current path setting is $PATH"
;;
6)echo "your current working directory is pwd"
;;
7)nousers=`who|wc -l`
;;
*)echo "enter valid option from 1-7"
exit
;;
esac
////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
EXERCISE-9
A)CURL

1.DOWNLOAD A SINGLE FILE
the following command will get the content of the URL and display it in the STDOUT
$curl htttp://www.centos.org
2.SAVE THE CURL OUTPUT TO A FILE
we can save the result of the curl command to a file by using -o/-o options.
-o(lower case 0)the result will be save in the file name.
3.FETCH MULTIPLE FILES AT A TIME
we can download multiple file in a singke short by specifying the URL's on the command
example:curl -o https://www.tutorials point.com/machine-learning/index.htnl
4.FOLLOW HTTP LOCATION HEADERSNWITH -LOPTION
by default CURL doesn't follow the HTTP location headers.It is also terned as redirects when a requestedweb has is move to another place,then an HTTP locaton header be sent as a respone all will the have where the actual 
web page is located.
examole:$curl-l http://www.google.com
5.CONTINVE/RESUME APREVIOUS DOWNLOAD
using curl-c option , you can continue a download which was stopped already for some reason this will be help full when you download large file and the download got interupted 
CURL -OHTTP://WWWW.gnu.org/softwarelgettext/manual/get text.html.

B)WGET

GNU WGET is a command line utiling for downloading file from the web with wgte ,you can download files using HTTP,HTTPS,and FTP protocals.Wget provides a number of options allowing
you to download multiple files,resume downloads ,limit the band width,recursion,downloads,download in the back ground ,mirror a website ,and much more
1.INSTALLING WGET ON LINUX
            sudo apt install wget
            syntax of command
            wget[option][url]
2.TO DOWNLOAD TAR.TZ FILE FROM CDN.KERNEL.ORG
ex1:wget http://cdn.kernel.org/pub linux/kernel/v4.x/linux-4.17.2.tax.xz
ex2:wdget http://www.gmail.com/
    it creates index.html
if the file already exists,wget will add.N(number) at the end of the file name
3.TO TURN OFF THE OUTPUT,USE THE -Q OPTION
example 3:wget -q http:///www.gmail.com/
4.TO SAVE THE DOWNLOAD FILE UNDER A DIFFERENT NAME ,PASS THE -O OPTION FOLLLOWED BY THE CHOSEN NAME
EXAMPLE :wget -o latest -h-ZIP http://github.com/gohgoio/hugo/archive/master.ZIP
the command above will same the latest hugo ZIP file from gihub as latest -hugozip insted of its original name.
5.creating a mirror of a website with wget,use the to create a minor of website with wget,use the -m option .This will create a complete to all copy of the website by following
and down loading all interval link as well as the web site resource(java script,css,images)

 Experiment-4:
echo "1.About your OS and version,release number,kernel version \n 2.Show all available shells \n 3.Show mouse setting \n 4.Show computer cpu informaton like processor type,speed etc \n 5.Show memory information \n 6.Show harddisk information like size of hard-disk,cache memory modeletc \n 7.File system (Mounted) \n 8.Keyboard setting"
echo "enter option"
read op
case $op in
1.)echo "OS and version,release number,kernel version"
if [ -f/etc/os-release ]
then
echo "OS :"
cat /etc/os-release
else
echo "enter valid option"
fi
;;
2.)echo "all avaible shells"
if [ -f/etc/shells ]
then
cat /etc/shells
else
echo "enter valid option"
fi
;;
3.)echo "mouse setting"
xinput -list-props "PixArt USB Optical Mouse"
;;
4.)echo "cpu information"
if [ -f/proc/cpuinfo ]
then
cat /proc/cpuinfo
else
echo "enter valid option"
fi
;;
5.)echo "memory information"
if [ -f/proc/meminfo ]
then
cat /proc/meminfo
else
echo "enter valid information"
fi
;;
6.)echo "hard disk information"
echo "Driver :"
if [ -f/proc/driver/rtc ]
then
cat /proc/driver/rtc
else
echo "enter valid option"
fi
;;
7.)echo "file system"
if [ -f/proc/mounts ]
then
cat /proc/mounts
else
echo "enter valid option"
fi
;;
8.)echo "Keyboard setting"
xinput -list-proc "Dell Dell USB Entey Keyboard"
;;
*)echo "enter valid option only"
;;
esac
_________________________________________________________________________________________________________________________________________________________________________
Experiment-5:
ch=1
while [ $ch -eq 1 ]
do
echo "enter two numbers"
read n1 n2
echo "1-addition\n 2-subtraction\n 3-multiplication\n 4-division\n 5-remainder"
echo "enter option"
read op
case $op in
1.)res= `expr $n1 + $n2 `
echo "addition of $n1 and $n2 is $res"
;;
2.)res= `expr $n1 - $n2 `
echo "subtraction of $n1 and $n2 is $res"
;;
3.)res= `expr $n1 \* $n2 `
echo "multiplication of $n1 and $n2 is $res"
;;
4.)res= `expr $n1 / $n2 `
echo "division of $n1 and $n2 is $res"
;;
5.)res= `expr $n1 % $n2 `
echo "remainder of $n1 and $n2 is $res"
;;
*)echo "enter valid option 1-5"
;;
esac
echo "enter choise to repeat 1-yes another value-no"
read ch
done
________________________________________________________________________________________________________________________________________________________________________________
Experiment-9:
grep
1.Case insensitive search :The -i option enables to search for a string case insensitively in the given file.It matches the word like "UNIX","Unix","unix".
Ex:~$ grep -i "cat" exp.txt
	for a word cat
	cat
	cat
2.Displaying the count of number of matches:We can find the no.of lines that matches the given word.
Ex:~$ grep -c "cat" exp.txt
	3
3.Display the file names that matches the pattern:We can just display the files that contains the given string.
Ex:~$ grep -l "cat" *
	grep:Desktop: Is a directory
	grep:Documents: Is a directory
	grep:Downloads:Is a directory
	exp4.sh
	exp4.sh~
	exp.txt
	hs-err-pid2272.log
	kd.sh
	kd.sh~
	grep:Music:Is a directory
	grep:Pictures:Is a directory  
	grep:Public:Is a directory
	grep:Templates:Is a directory
4.Checking for the Whole words in a file :By Default,grep matches the given string/pattern even if it found as a substring in a file.The -w option to grep makes only the whole words.
Ex:~$ grep -w "cat" exp.txt
	for a word cat
	cat is a animal
	cat drinks milk
5.Displaying only the matched pattern :By default ,grep displays the entire line which has the matched string.We can make the grep to display only the matched string by using the -o option.
Ex:~$ grep -o "cat" exp.txt
	cat
	cat
	cat
6.Show line number while displaying the output using grep -n:To show the line no.of file with the matched.
Ex:~$ grep -n "cat" exp.txt
	3:for a word cat
	4.cat is a animal 
	5.cat drinks milk
7.Inverting the pattern match:You can display the lines that are not matched with the specified search string pattern using -v option.
Ex:~$ grep -v "cat" exp.txt
	this is a sample program
	for searching word in a file
8.Matching the lines that start with a string :The ^ regular expression pattern specified the start of a line.
Ex:~$ grep "^cat" exp.txt
	cat is a animal
	cat drinks milk
9.Matching the lines that end with a string :The $ regular expression pattern specifies the end of a line.
Ex:~$ grep "cat$" exp.txt
	for a word cat
_________________________________________________________________________________________________________________________________________________________________________________________________________

  

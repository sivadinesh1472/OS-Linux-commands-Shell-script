# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT

![catfile1](./img1/01-catfile1.png)
cat < file2
## OUTPUT

![catfile2](./img1/02-catfile2.png)
# Comparing Files
cmp file1 file2
## OUTPUT
 ![cmpfile](./img1/04-cmp.png)
comm file1 file2
 ## OUTPUT

 ![commfile](./img1/04-comm.png)
diff file1 file2
## OUTPUT
![fifffile1](./img1/05-diff.png)
#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT


![catfil11](./img1/06-catfie11.png)


cut -d "|" -f 1 file22
## OUTPUT
![catfile22](./img1/07-file22.png)


cut -d "|" -f 2 file22
## OUTPUT

![catfile22](./img1/08-catfile22.png)

cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT

![catnewfile1](./img1/09-newfile.png)


grep hello newfile 
## OUTPUT

![grep hello newfile ](./img1/10-newfile.png)


grep -v hello newfile 
## OUTPUT

![grep -v hello newfile ](./img1/11.grep.png)

cat newfile | grep -i "hello"
## OUTPUT

![cat newfile | grep -i "hello"](./img1/12-catnewfile.png)


cat newfile | grep -i -c "hello"
## OUTPUT

![cat newfile | grep -i -c "hello"](./img1/13-catnew%20file.png)


grep -R ubuntu /etc
## OUTPUT

![grep -R ubuntu /etc](./img1/14-grep.png)

grep -w -n world newfile   
## OUTPUT

![grep -w -n world newfile ](./img1/15-grep.png)

cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT

![egrep -w 'Hello|hello' newfile ](./img1/16-egrep.png)

egrep -w '(H|h)ello' newfile 
## OUTPUT

![egrep -w '(H|h)ello' newfile ](./img1/17-grep.png)

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


![egrep-w](./img1/18-egrep.png)

egrep '(^hello)' newfile 
## OUTPUT

![egrep '(^hello)' newfile ](./img1/19-grep.png)

egrep '(world$)' newfile 
## OUTPUT

![egrep '(world$)' newfile ](./img1/20-world$.png)

egrep '(World$)' newfile 
## OUTPUT

![egrep '(World$)' newfile ](./img1/21-newfile.png)

egrep '((W|w)orld$)' newfile 
## OUTPUT

![egrep '((W|w)orld$)' newfile ](./img1/22-egrep.png)

egrep '[1-9]' newfile 
## OUTPUT

![egrep '[1-9]' newfile ](./img1/23-egrep.png)

egrep 'Linux.*world' newfile 
## OUTPUT

![egrep 'Linux.*world' newfile ](./img1/24-egrep.png)

egrep 'Linux.*World' newfile 
## OUTPUT

![egrep 'Linux.*World' newfile ](./img1/25-egrep.png)


egrep l{2} newfile
## OUTPUT

![egrep l{2} newfile](./img1/26-egrep.png)

egrep 's{1,2}' newfile
## OUTPUT 

![egrep 's{1,2}' newfile](./img1/27-grep.png)

cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT

![sed -n -e '3p' file23](./img1/28-sed.png)

sed -n -e '$p' file23

## OUTPUT
![sed -n -e '$p' file23](./img1/29-sed.png)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![sed  -e 's/Ram/Sita/' file23](./img1/30-sed.png)

sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![sed  -e '2s/Ram/Sita/' file23](./img1/31-sed.png)

sed  '/tom/s/5000/6000/' file23
## OUTPUT

![sed  '/tom/s/5000/6000/' file23](./img1/32-sed.png)

sed -n -e '1,5p' file23
## OUTPUT

![sed -n -e '1,5p' file23](./img1/33-sed.png)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![sed -n -e '2,/Joe/p' file23](./img1/34-sed.png)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![sed -n -e '/tom/,/Joe/p' file23](./img1/35-sed.png)

seq 10 
## OUTPUT

![seq10](./img1/36.png)

seq 10 | sed -n '4,6p'
## OUTPUT

![seq 10 | sed -n '4,6p'](./img1/37.png)

seq 10 | sed -n '2,~4p'
## OUTPUT

![seq 10 | sed -n '2,~4p'](./img1/38.png)

seq 3 | sed '2a hello'
## OUTPUT

![seq3](./img1/39-seq3.png)

seq 2 | sed '2i hello'
## OUTPUT

![seq2](./img1/40-seq2.png)

seq 10 | sed '2,9c hello'
## OUTPUT
![seq10](./img1/41-seq10.png)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![sed-n](./img1/42-sed.png)

sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

![ed -n '2,4{s/$/*/;p}' file23](./img1/43.png)

#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
![sort file21](./img1/44-sort.png)

cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT

![uniq](./img1/45-uniq.png)

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![cat file23 | tr [:lower:] [:upper:]](./img1/46-tr%20command.png)

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT

![caturlist](./img1/47-cat%20urlist.png)
 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![cat urllist.txt | tr -d ' ' | tr -s '.'](./img1/48-cat.png)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![backup](./img1/49-backup.png)

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

![tar-back](./img1/50-tar.png)


tar -xvf backup.tar
## OUTPUT

![tar -xvf backup.tar](./img1/51-tar.png)


gzip backup.tar

ls .gz
## OUTPUT
 ![ls](./img1/52-ls.png)
gunzip backup.tar.gz
## OUTPUT

 ![gunzip](./img1/53-gunzip.png					)
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 ![shell script](./img1/54%20script.png)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![cat herecheck.txt](./img1/55-cat-stop.png)

cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT

![bash](./img1/57-bash.png)
ls file1
## OUTPUT
![lsfile](./img1/56-ls%20file.png)
echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![echo](./img1/58-echo.pnga)
abcd
 
echo $?
 ## OUTPUT

![abcd](./img1/59-abcd.png)
 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT

![strcomp](./img1/60-strcomp.png)

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![strcomp](./img1/61-strcomp.png)

# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT
![psswdpern](./img1/62-pss.png)
# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT
![ifnested](./img1/63-ifnested.png)


# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT

![iftest](./img1/64-iftest.png)

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT
![ifnested](./img1/65-ifnested.png)
# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT
![elifcheck](./img1/66-elif.png)

# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
![ifcompound](./img1/67-ifcompound.png)

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
![casecheck](./img1/68-casecheck.png)

cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 
![chmod](./img1/69-chmod.png)
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 
 ![untiltest](./img1/70-until.png)
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
![chmod](./img1/71-chmod.png)
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 

![cat-forin](./img1/72-cat-forin.png)
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
dob
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 


![forin](./img1/73-forin.png)

cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 ![forin-3](./img1/74-forin3.png)

cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
![catforin](./img1/75-cat%20forin3.png)

cat forin3.sh

\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
$ ./forin3.sh

![catforin](./img1/76-catforin.png)

cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT

![cities](./img1/77-cities.png)

cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT
![c-style](./img1/78-c-style.png)
cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT
![forcetye](./img1/79-force%20type.png)
cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
![loop](./img1/80-loop.png)
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT
![iteration](./img1/81-iteration.png)

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
![number](./img1/82-number.png)
cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT
![name](./img1/83-name.png)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![name](./img1/84-name.png)


$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 

 
 ./funcex.sh 1 2
![echo](./img1/85-echo.png)
 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
 ~[arg](./img1/86-arg.png)
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 git 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 
 ![++](./img1/87-++.png)
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
![awk](./img1/88-awk.png)
cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 

![palindrome](./img1/89-palin.png)
# RESULT:
The Commands are executed successfully.

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
```https://private-user-images.githubusercontent.com/227094966/544909204-7f7c2fc1-fb12-417c-bccc-7cb83a46dad2.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NzAyMDI3MTMsIm5iZiI6MTc3MDIwMjQxMywicGF0aCI6Ii8yMjcwOTQ5NjYvNTQ0OTA5MjA0LTdmN2MyZmMxLWZiMTItNDE3Yy1iY2NjLTdjYjgzYTQ2ZGFkMi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjYwMjA0JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI2MDIwNFQxMDUzMzNaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT02NzIxZmMwNjg0ZjkzYmE3OTA3NGMwY2IyYWE2NWM5YTlkYzFiOWRiMDQ3ZjI2YjBiY2RmNTQ3YTEwYmNjMTNlJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.8O9ELLYvRdJACMrZv2e7EGP6aNS_N_FqNTetkP7XcbA
mehul
narayanan
^d
```
cat > file2
```
aishu
toji
^d
```
### Display the content of the files
cat < file1
## OUTPUT
```
mehul
narayan

```
cat < file2
## OUTPUT
```

aishu
toji

```
# Comparing Files
cmp file1 file2
## OUTPUT
```
file1 file2 differ: byte 1, line 1

``` 
comm file1 file2
 ## OUTPUT
```
	aishu
mehul
narayan
	toji


```
 
diff file1 file2
## OUTPUT
```
1,2c1,2
< mehul
< narayan
---
> aishu
> toji


```

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
```
hel
thi

```



cut -d "|" -f 1 file22
## OUTPUT
```
1001 
1002 
1003

```


cut -d "|" -f 2 file22
## OUTPUT
```
Ram 
tom 
Joe 
```

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
<img width="362" height="82" alt="image" src="https://github.com/user-attachments/assets/c0a713ba-03dc-4ba2-bf7b-944b3114f041" />



grep hello newfile 
## OUTPUT

<img width="346" height="78" alt="image" src="https://github.com/user-attachments/assets/eeeb72f8-b3f6-42ec-9a98-967b3869c777" />



grep -v hello newfile 
## OUTPUT

<img width="348" height="71" alt="image" src="https://github.com/user-attachments/assets/3ef058c3-6378-4815-92ad-4b94f2287883" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="441" height="100" alt="image" src="https://github.com/user-attachments/assets/876c8f21-ee04-4796-9ef5-6963a87f8341" />



cat newfile | grep -i -c "hello"
## OUTPUT
<img width="485" height="77" alt="image" src="https://github.com/user-attachments/assets/a0e5896f-c119-4390-97fb-7cb09d035b2a" />




grep -R ubuntu /etc
## OUTPUT

<img width="1354" height="947" alt="image" src="https://github.com/user-attachments/assets/8f58cb25-7fc2-4c69-b1a2-73bc5dd49896" />


grep -w -n world newfile   
## OUTPUT
<img width="607" height="78" alt="image" src="https://github.com/user-attachments/assets/f4f3f3a8-dbd1-4b90-98e4-25e6ba44f368" />


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
c
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT


<img width="161" height="43" alt="image" src="https://github.com/user-attachments/assets/4c5c9573-f268-43b2-ac06-335359c90695" />

egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="161" height="43" alt="image" src="https://github.com/user-attachments/assets/810c8dcf-6e4d-46ef-9ed0-a6d4ab8aabd3" />

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="161" height="43" alt="image" src="https://github.com/user-attachments/assets/54913ea1-89e2-413f-9efc-a35164ac7f49" />


egrep '(^hello)' newfile 
## OUTPUT


<img width="161" height="28" alt="image" src="https://github.com/user-attachments/assets/a3320be5-d44a-4adb-b432-24d33952f08a" />

egrep '(world$)' newfile 
## OUTPUT


<img width="162" height="44" alt="image" src="https://github.com/user-attachments/assets/db5123e3-73f7-45c6-b105-a92611a6313d" />

egrep '(World$)' newfile 
## OUTPUT

<img width="162" height="44" alt="image" src="https://github.com/user-attachments/assets/ddac6d2b-31d3-4534-8ce9-2d3fd0dc140a" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="316" height="69" alt="image" src="https://github.com/user-attachments/assets/b2c46535-4b5a-458c-ae1e-f604da739bff" />

egrep '[1-9]' newfile 
## OUTPUT

<img width="317" height="28" alt="image" src="https://github.com/user-attachments/assets/bb28c610-4e07-4b6d-96ce-81f6ece3a4dd" />

egrep 'Linux.*world' newfile 
## OUTPUT



<img width="317" height="28" alt="image" src="https://github.com/user-attachments/assets/94644706-cc4e-40f4-b5ab-85c304dc26aa" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="317" height="28" alt="image" src="https://github.com/user-attachments/assets/a576e550-cecd-45a3-bda9-fda5dfb57eae" />

egrep l{2} newfile
## OUTPUT


<img width="315" height="48" alt="image" src="https://github.com/user-attachments/assets/10cc8e51-cb9a-406d-8d88-63713ea13cf7" />

egrep 's{1,2}' newfile
## OUTPUT 

<img width="378" height="92" alt="image" src="https://github.com/user-attachments/assets/a1ddfdbe-ab51-453c-a086-6204b5502d79" />
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

```
1002 | tom |  5000 | Admin
```

sed -n -e '$p' file23
## OUTPUT

```
1001 | Ram | 10000 | HR
```

sed  -e 's/Ram/Sita/' file23
## OUTPUT
```
1001 | Sita | 10000 | HR
1001 | Sita | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Sita | 10000 | HR
```


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
```
1001 | Ram | 10000 | HR
1001 | Sita | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
```


sed  '/tom/s/5000/6000/' file23
## OUTPUT
```
1001 | Ram | 10000 | HR
1001 | Sita | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
```


sed -n -e '1,5p' file23
## OUTPUT

```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
```

sed -n -e '2,/Joe/p' file23
## OUTPUT

```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
```


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
```
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer

```


seq 10 
## OUTPUT
```
1
2
3
4
5
6
7
8
9
10

```


seq 10 | sed -n '4,6p'
## OUTPUT
```
4
5
6
```


seq 10 | sed -n '2,~4p'
## OUTPUT
```
2
3
4
```


seq 3 | sed '2a hello'
## OUTPUT
```
1
2
hello
3

```


seq 2 | sed '2i hello'
## OUTPUT
```
1
hello
2
```

seq 10 | sed '2,9c hello'
## OUTPUT
```

1
hello
10
```

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
```
$1001 | Ram | 10000 | HR
$1001 | Ram | 10000 | HR
$1002 | tom |  5000 | Admin

```


sed -n '2,4{s/$/*/;p}' file23


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
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1004 | Sit |  7000 | Dev
1005 | Sam |  5000 | HR
```

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

```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
```

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
```
1001 | RAM | 10000 | HR
1001 | RAM | 10000 | HR
1002 | TOM |  5000 | ADMIN
1003 | JOE |  7000 | DEVELOPER
1005 | SAM |  5000 | HR
1004 | SIT |  7000 | DEV
1003 | JOE |  7000 | DEVELOPER
1001 | RAM | 10000 | HR
```
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
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
```

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
```
``www.yahoo.com
www.google.com
www.mrcet.com`

```

#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="946" height="1005" alt="image" src="https://github.com/user-attachments/assets/c0019015-1d01-480a-a8dd-8097cbcd336d" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="946" height="1005" alt="image" src="https://github.com/user-attachments/assets/2142f04e-e752-441c-8a67-51c2e79ed803" />

tar -xvf backup.tar
## OUTPUT
<img width="946" height="1005" alt="image" src="https://github.com/user-attachments/assets/1ee5ebb1-2c6d-402d-937c-a2f1fbf84faa" />
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="471" height="89" alt="image" src="https://github.com/user-attachments/assets/90718a13-16dd-4895-ba4e-3a0bac7e64d7" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="471" height="89" alt="image" src="https://github.com/user-attachments/assets/e986b866-0084-47bb-b45d-50241e3b74a9" />


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
<img width="650" height="418" alt="image" src="https://github.com/user-attachments/assets/23af31d9-496f-4b2d-afc5-f34b955ef06e" />

 
ls file1
## OUTPUT
```
file1
```
echo $?
## OUTPUT 

```
127
```


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
<img width="646" height="250" alt="image" src="https://github.com/user-attachments/assets/d28bdced-d2e0-4cc7-aa72-5c00a898a5f8" />


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
<img width="450" height="35" alt="image" src="https://github.com/user-attachments/assets/63ddc8dc-a1ef-4b58-b5d9-14afe5d3a1d3" />

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
<img width="449" height="69" alt="image" src="https://github.com/user-attachments/assets/a35b47ce-e491-47eb-930d-7aa282b80de8" />



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
<img width="448" height="40" alt="image" src="https://github.com/user-attachments/assets/6fffc3e0-9a74-4801-a73f-2eff8207b9d5" />

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
<img width="359" height="63" alt="image" src="https://github.com/user-attachments/assets/8079b73e-d580-4e8b-a0a8-574010014ff1" />

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
<img width="459" height="45" alt="image" src="https://github.com/user-attachments/assets/0180d68f-aa30-484a-a3c7-00e792393d4b" />


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
<img width="301" height="35" alt="image" src="https://github.com/user-attachments/assets/d6ab3dae-e960-44e6-889d-ce89252e60e0" />

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
 #output

 <img width="457" height="45" alt="image" src="https://github.com/user-attachments/assets/b5c9e2bd-0b15-4f81-a359-153f1475749d" />

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
 <img width="458" height="244" alt="image" src="https://github.com/user-attachments/assets/5f0fd825-41ea-4cee-8546-f3d635d0d861" />

 
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
 <img width="554" height="141" alt="image" src="https://github.com/user-attachments/assets/98641c44-24dd-421a-8c20-fbc660c6f525" />

 
 
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
 <img width="629" height="198" alt="image" src="https://github.com/user-attachments/assets/e4222ab2-8025-41c9-848a-20d50c47df36" />

 
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
 <img width="633" height="134" alt="image" src="https://github.com/user-attachments/assets/d3e2bbc9-d70e-454b-9df4-46481025668f" />

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
 
$ ./forin2.sh 
 <img width="633" height="134" alt="image" src="https://github.com/user-attachments/assets/72827a21-6713-472b-aa67-64f64e405de0" />

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
<img width="629" height="198" alt="image" src="https://github.com/user-attachments/assets/9f849406-1654-4420-815b-257a6ad355c4" />



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

<img width="629" height="198" alt="image" src="https://github.com/user-attachments/assets/7f81ab3a-ee4b-4797-9b0a-b5e4abc9147d" />

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
<img width="633" height="134" alt="image" src="https://github.com/user-attachments/assets/62fdd41d-da26-41ad-b649-a62b50883849" />

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
<img width="633" height="134" alt="image" src="https://github.com/user-attachments/assets/bc8c46ed-6e16-4247-a72f-89169635c617" />

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
<img width="639" height="204" alt="image" src="https://github.com/user-attachments/assets/04136392-b4d3-4be7-b805-34705c213147" />

 
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
<img width="637" height="161" alt="image" src="https://github.com/user-attachments/assets/e6dc102f-fd6f-45bc-bda5-89c5f82a4b81" />

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
 <img width="636" height="178" alt="image" src="https://github.com/user-attachments/assets/4388efdc-606b-4e18-8226-1b9305ae495c" />

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
<img width="626" height="138" alt="image" src="https://github.com/user-attachments/assets/56a06e69-b332-4d7a-8210-dccbf3943315" />



 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="629" height="288" alt="image" src="https://github.com/user-attachments/assets/e381c2a8-4580-4edb-bc7a-c520431dcc93" />


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
 ./funcex.sh <img width="653" height="49" alt="image" src="https://github.com/user-attachments/assets/791f2f18-10b4-4ca6-b498-1081b773e19b" />


 
 ./funcex.sh 1 2<img width="653" height="49" alt="image" src="https://github.com/user-attachments/assets/f8d70598-df8d-43c4-af69-cd52813b3256" />


 
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

<img width="656" height="90" alt="image" src="https://github.com/user-attachments/assets/64a56b54-8dd4-4f41-a260-8c0be27e61b0" />

$ ./argshift.sh 1 2 3
 
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
<img width="656" height="90" alt="image" src="https://github.com/user-attachments/assets/c7384ff1-6577-47db-a0e2-17341ed76804" />

$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3

 <img width="656" height="330" alt="image" src="https://github.com/user-attachments/assets/ad86aaf7-5658-44e0-a51b-745009406701" />

 
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

 <img width="654" height="315" alt="image" src="https://github.com/user-attachments/assets/c16b98d4-446f-470f-848c-b02104d73ba4" />

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
<img width="655" height="93" alt="image" src="https://github.com/user-attachments/assets/adc2ef10-ab38-40b2-a893-9bff542513ef" />


# RESULT:
The Commands are executed successfully.

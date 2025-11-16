# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting
# Developed by: V.SHRIYHA
# Register NO.:212224230267
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

![image](https://github.com/user-attachments/assets/6164177f-84dc-44a8-9a62-575a570064a0)


cat < file2
## OUTPUT

![image](https://github.com/user-attachments/assets/b31bc72c-0e37-49b6-924b-bb62b898eaba)


# Comparing Files
cmp file1 file2
## OUTPUT

![Screenshot 2025-04-23 134834](https://github.com/user-attachments/assets/4e02c9eb-5fba-417e-b9a7-5918ba3232a3)

 
comm file1 file2
 ## OUTPUT

![image](https://github.com/user-attachments/assets/7194e5d9-75b9-4b8b-afd2-086402c5d335)

 
diff file1 file2
## OUTPUT

![image](https://github.com/user-attachments/assets/57a8e4c4-190c-42f6-a5c2-b430bdfddb98)


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

![image](https://github.com/user-attachments/assets/8de1301b-c764-4c8b-9ffa-c3c8b5704d20)



cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/user-attachments/assets/bfceb031-ef33-40a4-9bdb-805c390f8fee)


cut -d "|" -f 2 file22
## OUTPUT

![image](https://github.com/user-attachments/assets/ec647ff4-746d-4434-ad58-33a8390ff932)


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

![image](https://github.com/user-attachments/assets/927702ed-5dc9-42a2-80d1-14e5477b0fe9)


grep hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/06353a5a-57b2-481f-857e-605ba093c16f)



grep -v hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/ba61deac-e229-419c-83f9-c547455634b1)


cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/cbb59b08-d91c-4f97-a40d-974b5524749a)



cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/76fd9499-2f19-455a-bde5-bdd8c1ff11c0)



grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT

![image](https://github.com/user-attachments/assets/0275227e-0264-401b-9a4e-9e5be2685cf3)


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

![image](https://github.com/user-attachments/assets/9b3bf337-6468-4375-83df-ff6cc030c2b1)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/9bbaa507-3593-47d1-9c5e-d10f5df3577d)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/01ecc0a6-e76a-4f00-867f-830a5cba13d4)



egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/0f284118-0db0-4184-b188-b02ecaf67978)


egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/f33e9116-1def-4cf8-9293-4c0e28c08c9b)


egrep '(World$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/a1964b8e-1053-4d1b-8bc4-69e7467237da)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/6007844a-0131-47f6-8884-3a6fcc578d96)


egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/41d214dc-7f23-447c-8f87-94752b232a31)


egrep 'Linux.*world' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/e7c42ab7-66dc-41d8-9b8a-a8aa5f75c6d9)

egrep 'Linux.*World' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/1df85d99-9be3-4e83-a54f-72cf01bc57ed)


egrep l{2} newfile
## OUTPUT

![image](https://github.com/user-attachments/assets/e178201b-9a48-4985-9818-7226bf88cf48)


egrep 's{1,2}' newfile
## OUTPUT 

![image](https://github.com/user-attachments/assets/bc8ffe5d-d388-4dae-81a9-c6981cfc88a9)


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

![image](https://github.com/user-attachments/assets/6c1b99b8-df72-49e5-b381-c53a7c54b8f7)


sed -n -e '$p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/f9ca531d-0d92-4404-84b2-3d422b2b3079)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/92d456f1-f98a-4b5d-98a9-5c2a8a3e0eb0)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/7211144b-8b9d-4779-bb65-a85afe6670f7)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/5623d065-6dbc-43b1-9ae5-72696866c25d)


sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/8d6e6f9f-3a4a-4761-8af8-d94f60525f1d)


sed -n -e '2,/Joe/p' file23
## OUTPUT


![Screenshot 2025-04-23 141401](https://github.com/user-attachments/assets/0e81d887-4349-4ef8-909e-bd42f20c25ca)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/069a8b73-9176-4504-abcf-0bb56b07d45a)


seq 10 
## OUTPUT



seq 10 | sed -n '4,6p'
## OUTPUT


![image](https://github.com/user-attachments/assets/9a5065e0-82c6-46a5-89f7-2917871381dd)


seq 10 | sed -n '2,~4p'
## OUTPUT


![image](https://github.com/user-attachments/assets/affb1487-532d-4d38-9df3-f5c282dde73a)


seq 3 | sed '2a hello'
## OUTPUT


![image](https://github.com/user-attachments/assets/0c9a2b2c-6dd5-4439-bd9f-317e89468e44)


seq 2 | sed '2i hello'
## OUTPUT


![image](https://github.com/user-attachments/assets/5f2b573f-9a39-41fa-b9fa-0e0753b2251f)


seq 10 | sed '2,9c hello'
## OUTPUT


![image](https://github.com/user-attachments/assets/3d41db03-2509-48e8-a8be-7057d07fe440)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/f0715d02-b416-4abe-b794-0d3207e1ccaa)


sed -n '2,4{s/$/*/;p}' file23


![image](https://github.com/user-attachments/assets/dd428929-9aee-4fb3-8f63-d926d07f528b)


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


![image](https://github.com/user-attachments/assets/4c1da12b-3c3d-48f7-9aee-7f291ad705e6)

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


![image](https://github.com/user-attachments/assets/61ca8213-f2a4-44e0-b9af-9f19d343bd2a)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 

![image](https://github.com/user-attachments/assets/4035f191-40dc-475c-bb33-5cdb1afd8f16)

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


![image](https://github.com/user-attachments/assets/6cd5089a-94f5-4996-8d39-18317e651b56)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT


![image](https://github.com/user-attachments/assets/f6f01f86-e304-43a9-a107-4d359a7a61fe)


#Backup commands
tar -cvf backup.tar *
## OUTPUT


![image](https://github.com/user-attachments/assets/e702aa86-a91b-4eca-b296-2747568ffb71)


![image](https://github.com/user-attachments/assets/b46fd125-efde-43c2-b911-b93b7d3ae0e9)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT


![image](https://github.com/user-attachments/assets/fa019f31-2d89-4165-b500-4b1f4b990063)


![image](https://github.com/user-attachments/assets/e99d28a8-fe10-43ac-9cd9-43d5cf388e51)

tar -xvf backup.tar
## OUTPUT


![image](https://github.com/user-attachments/assets/73cb209e-f01b-4cee-8808-746f99106cc7)


gzip backup.tar

ls .gz
## OUTPUT
gunzip backup.tar.gz
## OUTPUT


![image](https://github.com/user-attachments/assets/c0a11ec6-f21d-43c9-953a-746edcd07e81)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT


 ![image](https://github.com/user-attachments/assets/197b9407-831f-4762-90cf-95b6966a4686)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


![image](https://github.com/user-attachments/assets/bd9fde28-1da7-462a-84b9-aa20288b6ec7)

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


![image](https://github.com/user-attachments/assets/7924db36-e569-4c4b-8140-c7367c7aaf7e)
 
ls file1
## OUTPUT


![image](https://github.com/user-attachments/assets/7f6a819a-3769-4888-9093-c8f328c42bcd)


echo $?
## OUTPUT 


![image](https://github.com/user-attachments/assets/5907aebf-482a-4171-8a81-e44300857ec7)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 


 ![image](https://github.com/user-attachments/assets/72dfb2f8-1a2b-4cfa-b201-e329c85f5a18)

abcd
 
echo $?

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


![image](https://github.com/user-attachments/assets/4d4af819-8a93-4eb3-9d74-7b4dc7e2682c)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


![image](https://github.com/user-attachments/assets/abdb3cd5-232f-440f-9402-0ed39a6f6a8d)


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


![image](https://github.com/user-attachments/assets/c719aa06-d75c-4bae-b12e-f90eb6a1020b)


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


![image](https://github.com/user-attachments/assets/28f7a6a6-ecaf-42f5-848d-616e2549d2cb)


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


![image](https://github.com/user-attachments/assets/056340a8-88b0-4211-9353-d33ef1154435)

![image](https://github.com/user-attachments/assets/f6c4ff0b-f71f-4efa-ad9b-ad0447164368)


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


![image](https://github.com/user-attachments/assets/0254612e-03c3-477f-94c4-c75dc0b8da61)


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


![image](https://github.com/user-attachments/assets/1485336d-7f38-4a8f-8ec9-7fdde9dcfe1c)

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


![image](https://github.com/user-attachments/assets/da1e6f41-b7f5-4629-a72a-3f4266fc5218)


# RESULT:
The Commands are executed successfully.

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

<img width="572" height="112" alt="Screenshot from 2025-08-25 21-45-43" src="https://github.com/user-attachments/assets/95ef48a1-e727-4628-b305-374eeb4de620" />

cat < file2

## OUTPUT


<img width="573" height="104" alt="Screenshot from 2025-08-25 21-45-14" src="https://github.com/user-attachments/assets/bb7e8c14-6717-4dd1-be57-344294450e11" />


# Comparing Files

cmp file1 file2

## OUTPUT

 <img width="580" height="41" alt="Screenshot from 2025-08-26 10-45-16" src="https://github.com/user-attachments/assets/6d45f9b5-8f61-49f4-a97c-82384c1a0ea4" />

comm file1 file2

 ## OUTPUT

<img width="583" height="225" alt="Screenshot from 2025-08-26 10-48-48" src="https://github.com/user-attachments/assets/7eada5de-853c-43ec-94f5-6aee1f10b667" />

 
diff file1 file2

## OUTPUT

<img width="577" height="179" alt="Screenshot from 2025-08-26 10-50-06" src="https://github.com/user-attachments/assets/09dde345-f8c4-4728-ba4e-17dd6213502a" />


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

<img width="549" height="83" alt="Screenshot from 2025-08-26 11-34-40" src="https://github.com/user-attachments/assets/2b541c34-1cdd-4c2a-bb08-3416699a11dd" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="561" height="100" alt="Screenshot from 2025-08-26 11-35-17" src="https://github.com/user-attachments/assets/6d139450-e066-4b18-baa6-ae8fdfc3dd65" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="561" height="96" alt="Screenshot from 2025-08-26 11-36-11" src="https://github.com/user-attachments/assets/23df6fe1-3fcb-40a5-be6c-a1cb43e28fbd" />


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

<img width="561" height="48" alt="Screenshot from 2025-08-26 11-37-07" src="https://github.com/user-attachments/assets/bdce97b7-7814-4f7a-bf8a-4432e54493c4" />


grep hello newfile 
## OUTPUT

<img width="561" height="40" alt="Screenshot from 2025-08-26 11-38-45" src="https://github.com/user-attachments/assets/8131a89b-ead0-45ab-994c-1e2c0eb38057" />



grep -v hello newfile 
## OUTPUT

<img width="557" height="54" alt="image" src="https://github.com/user-attachments/assets/14136a7a-e49b-4a9b-a573-a465df5c9ced" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="612" height="56" alt="image" src="https://github.com/user-attachments/assets/9a7ea828-01aa-47e6-af8f-a7d4b8b1e1ad" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="648" height="41" alt="image" src="https://github.com/user-attachments/assets/159c2571-e1a2-4719-af4e-a947b1c932c9" />



grep -R ubuntu /etc
## OUTPUT

<img width="1853" height="745" alt="Screenshot from 2025-08-26 11-32-19" src="https://github.com/user-attachments/assets/cae9bfa5-c526-4823-896a-13466633109c" />


grep -w -n world newfile   
## OUTPUT

<img width="645" height="59" alt="image" src="https://github.com/user-attachments/assets/0f0b944f-c10d-4944-ae57-dcffc49d1dcd" />


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

<img width="649" height="61" alt="image" src="https://github.com/user-attachments/assets/0dca63dd-f5bd-438e-a593-0fc63e8f3872" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="649" height="61" alt="image" src="https://github.com/user-attachments/assets/6d189091-a67a-464e-8c30-4e743d3c3d32" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="649" height="61" alt="image" src="https://github.com/user-attachments/assets/b9060bd1-3b17-4fff-87c1-6048477e42e8" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="649" height="43" alt="image" src="https://github.com/user-attachments/assets/a8b300a6-598f-4b2c-a6be-cfdbe6d79f57" />


egrep '(world$)' newfile 
## OUTPUT

<img width="649" height="43" alt="image" src="https://github.com/user-attachments/assets/33473d56-b2cf-4f7b-975c-04d3918b461c" />


egrep '(World$)' newfile 
## OUTPUT

<img width="649" height="37" alt="image" src="https://github.com/user-attachments/assets/9b818466-927b-4f54-b858-a63671e3d0d8" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="659" height="78" alt="image" src="https://github.com/user-attachments/assets/38f10b48-a666-4cf3-8f4f-d0f1e04fe89a" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="666" height="41" alt="image" src="https://github.com/user-attachments/assets/f8d2414d-ac1d-476b-b64f-dbfed478b14e" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="666" height="41" alt="image" src="https://github.com/user-attachments/assets/ca126efe-f378-4503-b944-db01e099ca7b" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="666" height="41" alt="image" src="https://github.com/user-attachments/assets/7b33bfd4-282a-43f2-aee8-eb38f2fae684" />


egrep l{2} newfile
## OUTPUT
<img width="666" height="55" alt="image" src="https://github.com/user-attachments/assets/af71c03c-df93-417c-b46a-497d4a1a40d3" />



egrep 's{1,2}' newfile
## OUTPUT 

<img width="666" height="76" alt="image" src="https://github.com/user-attachments/assets/09d7bd55-2eed-4a97-8663-1fbe2c2ebd6f" />


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
<img width="540" height="40" alt="image" src="https://github.com/user-attachments/assets/9edb7686-ed3b-454e-bc63-8c19bd46e64e" />



sed -n -e '$p' file23
## OUTPUT
<img width="533" height="39" alt="image" src="https://github.com/user-attachments/assets/0005187d-7f8e-4c57-a122-a475f65933a2" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT


<img width="590" height="187" alt="image" src="https://github.com/user-attachments/assets/7a87871e-dae5-4ebf-86e2-28c7e6dcf02f" />

sed  -e '2s/Ram/Sita/' file23
## OUTPUT


<img width="599" height="183" alt="image" src="https://github.com/user-attachments/assets/6197b68c-9a92-48b1-ab70-0389714cbe31" />

sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="619" height="186" alt="image" src="https://github.com/user-attachments/assets/2dbcfd23-8b41-4e78-a223-e1262ebd4a1b" />


sed -n -e '1,5p' file23
## OUTPUT


<img width="556" height="113" alt="image" src="https://github.com/user-attachments/assets/e8dafab0-5ea7-4914-8196-d8e94845d34d" />

sed -n -e '2,/Joe/p' file23
## OUTPUT



<img width="591" height="81" alt="image" src="https://github.com/user-attachments/assets/4259e8d5-a75d-425e-a049-6bd9b27fcf24" />

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="619" height="60" alt="image" src="https://github.com/user-attachments/assets/7a26afa0-6c69-4811-ae8c-8075e1691584" />


seq 10 
## OUTPUT

<img width="402" height="200" alt="image" src="https://github.com/user-attachments/assets/57dc65ed-eac8-4e24-b5be-04f1375d1154" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="542" height="82" alt="image" src="https://github.com/user-attachments/assets/c8c18a30-cce3-44f6-946d-4e0d38048fa2" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="544" height="76" alt="image" src="https://github.com/user-attachments/assets/a585a9ae-4fb8-414c-a7a8-5b163716fa4a" />



seq 3 | sed '2a hello'
## OUTPUT


<img width="544" height="98" alt="image" src="https://github.com/user-attachments/assets/0beb501b-62d5-4721-ab25-23c080561339" />

seq 2 | sed '2i hello'
## OUTPUT

<img width="545" height="80" alt="image" src="https://github.com/user-attachments/assets/a88cc05d-e66b-423b-9577-69fe3cffe6ab" />

seq 10 | sed '2,9c hello'
## OUTPUT
  
  
<img width="571" height="80" alt="image" src="https://github.com/user-attachments/assets/008e3b77-c9a8-4764-86e9-79937c936984" />
>


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="608" height="80" alt="image" src="https://github.com/user-attachments/assets/bf30a74f-70cd-47e3-b7b6-a31c7f735a17" />


sed -n '2,4{s/$/*/;p}' file23

<img width="604" height="77" alt="image" src="https://github.com/user-attachments/assets/2e95b8ab-aa71-494d-864e-7463dc3d44b3" />


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

<img width="445" height="116" alt="image" src="https://github.com/user-attachments/assets/279507b8-bdee-4bc6-a6b4-5dac9f2df6aa" />


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

<img width="656" height="184" alt="image" src="https://github.com/user-attachments/assets/3402da4f-6bf3-4ad9-8fc8-131d78bb1e5c" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="656" height="184" alt="image" src="https://github.com/user-attachments/assets/fdcc5cf3-f1bb-4212-bee8-192dbd5a4ce6" />

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

<img width="569" height="96" alt="image" src="https://github.com/user-attachments/assets/c3a4a417-e9f9-4f9e-a447-7a2bce8bf93d" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="697" height="94" alt="image" src="https://github.com/user-attachments/assets/101ea7f0-2cdb-466c-ba56-d0a504498ba5" />

#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="531" height="817" alt="image" src="https://github.com/user-attachments/assets/e4d376bf-790d-4314-a7c5-40b2544879ba" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="1128" height="1068" alt="image" src="https://github.com/user-attachments/assets/5adb07f3-e063-41d9-90b9-bbf7a5cf4ea2" />

tar -xvf backup.tar
## OUTPUT

<img width="605" height="1049" alt="image" src="https://github.com/user-attachments/assets/a2f0c712-d20b-40bd-b748-57fff5bebe2f" />


gzip backup.tar

ls .gz
## OUTPUT


 <img width="499" height="43" alt="image" src="https://github.com/user-attachments/assets/508cae2e-3381-4f1a-88a5-acce06c05b82" />

gunzip backup.tar.gz
## OUTPUT
<img width="1822" height="41" alt="image" src="https://github.com/user-attachments/assets/50362c6f-a98a-4ef3-9252-0c64f229717d" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="646" height="168" alt="image" src="https://github.com/user-attachments/assets/2fc9282d-94ab-45f0-90d0-d2abace481d5" />

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

 <img width="631" height="313" alt="image" src="https://github.com/user-attachments/assets/8c09429d-2a1b-44ba-bfe2-2d04e33d7119" />

ls file1
## OUTPUT
<img width="515" height="44" alt="image" src="https://github.com/user-attachments/assets/6dcc2375-f508-455e-b482-84d6e8f6392e" />

echo $?
## OUTPUT 

<img width="501" height="44" alt="image" src="https://github.com/user-attachments/assets/5522679f-84f8-40bf-9469-8a1bb081f5a5" />

./one
bash: ./one: Permission denied


 
echo $?
## OUTPUT 

<img width="501" height="44" alt="image" src="https://github.com/user-attachments/assets/e7f2d8f5-9286-4d44-b15f-ab905c7cf862" />

 
abcd
 
echo $?
 ## OUTPUT

<img width="504" height="185" alt="image" src="https://github.com/user-attachments/assets/a7c1ecad-2ffa-41b2-a6a4-bd17e0141344" />

 
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

<img width="569" height="401" alt="image" src="https://github.com/user-attachments/assets/6b6dbd2d-3a91-4f90-ba6d-725a938bbacb" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="621" height="99" alt="image" src="https://github.com/user-attachments/assets/810b2777-6c54-4c08-a2e7-b8ea583c5ede" />

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
<img width="471" height="40" alt="image" src="https://github.com/user-attachments/assets/11758b67-d93d-4d07-b141-99b76e22ec8f" />

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

<img width="467" height="43" alt="image" src="https://github.com/user-attachments/assets/7696d1e2-8707-4524-8520-b79564c6ab11" />


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
<img width="571" height="79" alt="image" src="https://github.com/user-attachments/assets/84ceb48b-625f-4dc1-aa78-de3e93f98b6a" />


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
<img width="571" height="79" alt="image" src="https://github.com/user-attachments/assets/867e9493-a374-4b4a-acb6-7de999faa425" />


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

<img width="577" height="80" alt="image" src="https://github.com/user-attachments/assets/01c674ca-e386-4766-a50b-37283e564327" />


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


 <img width="549" height="59" alt="image" src="https://github.com/user-attachments/assets/de0b5b43-7f0a-46e5-b01b-9534650ba1f2" />


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

 <img width="551" height="222" alt="image" src="https://github.com/user-attachments/assets/52926c81-0a60-490b-91d3-e3f68ce4aac5" />

 
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

 OUTPUT:

 <img width="548" height="133" alt="image" src="https://github.com/user-attachments/assets/033427b4-d237-4c8c-b44d-4e286950e6da" />

 OUTPUT
 
 <img width="548" height="133" alt="image" src="https://github.com/user-attachments/assets/32eae042-e422-4c48-8098-b4b3f9aa1cb2" />

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

OUTPUT
 
 <img width="547" height="183" alt="image" src="https://github.com/user-attachments/assets/65cf4b3e-f309-4547-9186-b36fbd8065a7" />

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
 <img width="549" height="134" alt="image" src="https://github.com/user-attachments/assets/8dc160a3-75f8-48d8-9ab5-a164c7872aaf" />

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

<img width="542" height="132" alt="image" src="https://github.com/user-attachments/assets/8ed5d8ae-9fb6-4689-86b4-10687dfd12cc" />


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


<img width="542" height="132" alt="image" src="https://github.com/user-attachments/assets/a2726fe2-4693-4b1f-9956-a4b2fd3488ce" />

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
<img width="551" height="256" alt="image" src="https://github.com/user-attachments/assets/e1b505ba-4edb-4148-a769-f7d038a61539" />

 
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
<img width="626" height="116" alt="image" src="https://github.com/user-attachments/assets/e4ecf2b7-3e2d-4299-8393-dd3423304e49" />

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
 <img width="655" height="152" alt="image" src="https://github.com/user-attachments/assets/b5742c7e-f643-4bdb-9f10-17602c4dd0a0" />

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


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



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

 <img width="513" height="166" alt="image" src="https://github.com/user-attachments/assets/a11a6c98-a208-4ed9-b1d4-453c7bf860fb" />

 ./funcex.sh 1 2

 <img width="513" height="166" alt="image" src="https://github.com/user-attachments/assets/3ceb0f9f-e25d-428f-9783-710f5b609c89" />

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

<img width="534" height="97" alt="image" src="https://github.com/user-attachments/assets/7e57af87-39fb-47bc-84c0-e801acee1a67" />

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

<img width="520" height="279" alt="image" src="https://github.com/user-attachments/assets/27883189-5ccd-480d-b08f-d5f42b5571ab" />


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
./argshift.sh 1 2 3
## OUTPUT
 
 <img width="520" height="279" alt="image" src="https://github.com/user-attachments/assets/45b92877-d43d-49f8-b67a-8428823167e4" />

 
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
 <img width="541" height="256" alt="image" src="https://github.com/user-attachments/assets/a23b832c-77d5-4eae-90fc-7e1d9ba4c38e" />

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

<img width="552" height="97" alt="image" src="https://github.com/user-attachments/assets/af2e939c-9ab0-4aa5-90f6-ada74e0c3726" />

# RESULT:
The Commands are executed successfully.

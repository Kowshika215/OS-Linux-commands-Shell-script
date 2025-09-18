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

<img width="285" height="178" alt="Screenshot 2025-09-11 142009" src="https://github.com/user-attachments/assets/63459cc9-6121-4c08-98ba-af55d13a9015" />


cat < file2
## OUTPUT

<img width="251" height="177" alt="Screenshot 2025-09-11 142158" src="https://github.com/user-attachments/assets/9bda7fb4-1db4-4515-807c-5ea88517a2b1" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="381" height="78" alt="Screenshot 2025-09-11 142338" src="https://github.com/user-attachments/assets/6301b1e3-a406-4f6d-97dd-a9f415ddff86" />

comm file1 file2
 ## OUTPUT
<img width="434" height="270" alt="Screenshot 2025-09-11 142432" src="https://github.com/user-attachments/assets/3b0912b4-80b7-43b5-a862-9a26815ec465" />

 
diff file1 file2
## OUTPUT

<img width="427" height="351" alt="Screenshot 2025-09-11 142508" src="https://github.com/user-attachments/assets/da6cfda2-bdc4-4f40-9a54-bac6e7da1194" />

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

<img width="312" height="172" alt="Screenshot 2025-09-11 142543" src="https://github.com/user-attachments/assets/f1b66ed9-8d59-4e5e-8e41-110d5de8ad5d" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="305" height="178" alt="Screenshot 2025-09-11 142628" src="https://github.com/user-attachments/assets/69b05c2e-aa40-4fec-ac8a-e540742165bd" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="348" height="171" alt="Screenshot 2025-09-11 142703" src="https://github.com/user-attachments/assets/b616438f-5192-4045-a6b6-591da3dc7fe9" />


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
<img width="357" height="79" alt="Screenshot 2025-09-11 143757" src="https://github.com/user-attachments/assets/38749e03-54c4-44b7-b302-69754f73aed3" />




grep hello newfile 
## OUTPUT

<img width="357" height="79" alt="Screenshot 2025-09-11 143757" src="https://github.com/user-attachments/assets/caf155ec-3982-44f5-887b-4727315cec35" />




grep -v hello newfile 
## OUTPUT

<img width="359" height="80" alt="Screenshot 2025-09-11 143821" src="https://github.com/user-attachments/assets/a5edffa9-03e8-41e6-a9e1-ea895c6c4e71" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="439" height="78" alt="Screenshot 2025-09-11 143921" src="https://github.com/user-attachments/assets/9f31cc67-54e7-435d-8c52-e54887a447c0" />



cat newfile | grep -i -c "hello"
## OUTPUT


<img width="508" height="77" alt="Screenshot 2025-09-11 143953" src="https://github.com/user-attachments/assets/40febf32-a1d2-4c2c-a634-56af57ca872d" />


grep -R ubuntu /etc
## OUTPUT

<img width="949" height="327" alt="Screenshot 2025-09-11 143558" src="https://github.com/user-attachments/assets/c16b7d5e-dccc-4769-8ef3-e3f05f21b3e6" />


grep -w -n world newfile   
## OUTPUT

<img width="383" height="79" alt="Screenshot 2025-09-11 144204" src="https://github.com/user-attachments/assets/9f53be1e-f200-4b28-b2f8-7dbce5a0bbfd" />

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

<img width="448" height="82" alt="Screenshot 2025-09-11 144248" src="https://github.com/user-attachments/assets/9418ff63-dc16-450a-8811-ffb827191b28" />


egrep -w '(H|h)ello' newfile 
## OUTPUT



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="404" height="75" alt="Screenshot 2025-09-13 104657" src="https://github.com/user-attachments/assets/3ae09a40-f089-4a92-9f67-d4d67c213499" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="356" height="79" alt="Screenshot 2025-09-13 132321" src="https://github.com/user-attachments/assets/1e5df430-0783-4a4d-b993-197bb0550681" />



egrep '(world$)' newfile 
## OUTPUT
<img width="357" height="81" alt="Screenshot 2025-09-13 132457" src="https://github.com/user-attachments/assets/b0e59036-9570-4b28-9451-92bf64881843" />



egrep '(World$)' newfile 
## OUTPUT

<img width="357" height="81" alt="Screenshot 2025-09-13 132457" src="https://github.com/user-attachments/assets/2396b293-12cb-40c0-a2f8-313d9cb4a246" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="389" height="79" alt="Screenshot 2025-09-13 132552" src="https://github.com/user-attachments/assets/c3bda850-6298-45ed-b48f-7c9cfc8070c4" />

egrep '[1-9]' newfile 
## OUTPUT

<img width="345" height="57" alt="Screenshot 2025-09-13 132640" src="https://github.com/user-attachments/assets/bd39d727-1af9-48a4-9f5c-6d3ad7fea202" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="381" height="50" alt="Screenshot 2025-09-13 132722" src="https://github.com/user-attachments/assets/62eb1c2b-92d6-4566-91a4-ba79d3a52272" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="381" height="50" alt="Screenshot 2025-09-13 132722" src="https://github.com/user-attachments/assets/5dc2aab7-6d71-411c-8be6-5fca6255a894" />

egrep l{2} newfile
## OUTPUT

<img width="333" height="50" alt="Screenshot 2025-09-13 132753" src="https://github.com/user-attachments/assets/445dbe76-d4fd-4eeb-8b6f-0eb155aded76" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="358" height="51" alt="Screenshot 2025-09-13 132829" src="https://github.com/user-attachments/assets/c2186a6d-865b-4cb7-bd4e-327242a29736" />

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

<img width="343" height="51" alt="Screenshot 2025-09-13 133559" src="https://github.com/user-attachments/assets/0351c19d-8e16-460c-9ff3-40aaf11547f1" />


sed -n -e '$p' file23
## OUTPUT

<img width="348" height="77" alt="Screenshot 2025-09-13 133909" src="https://github.com/user-attachments/assets/c5a463fc-73d2-446c-b0ad-d2a72c899a9f" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="446" height="253" alt="Screenshot 2025-09-13 133816" src="https://github.com/user-attachments/assets/dc247023-e9c8-40c0-9e09-31440ef8803b" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="496" height="248" alt="Screenshot 2025-09-13 134040" src="https://github.com/user-attachments/assets/98c7c9b0-354e-4128-a53e-d77755b75a4b" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="450" height="251" alt="Screenshot 2025-09-13 134124" src="https://github.com/user-attachments/assets/602b779a-6175-4d2b-bc0b-aaf2eec6f92a" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="387" height="182" alt="Screenshot 2025-09-13 134209" src="https://github.com/user-attachments/assets/513bc39b-814f-41ce-826a-eaf31adb90d9" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="365" height="127" alt="Screenshot 2025-09-13 134357" src="https://github.com/user-attachments/assets/b092756a-64cb-44a7-a9b2-b977fe3c5797" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


<img width="466" height="96" alt="Screenshot 2025-09-13 134523" src="https://github.com/user-attachments/assets/7f7db690-77c9-4b1f-b70c-07c3234eff8e" />


seq 10 
## OUTPUT


<img width="284" height="307" alt="Screenshot 2025-09-13 134549" src="https://github.com/user-attachments/assets/9c84f45a-4016-4f5e-bc03-fe679cb20443" />


seq 10 | sed -n '4,6p'
## OUTPUT


<img width="359" height="129" alt="Screenshot 2025-09-13 134625" src="https://github.com/user-attachments/assets/f4fc80f6-3e18-40bb-a24c-33988a8b3d4e" />


seq 10 | sed -n '2,~4p'
## OUTPUT



seq 3 | sed '2a hello'
## OUTPUT


<img width="327" height="145" alt="Screenshot 2025-09-13 134659" src="https://github.com/user-attachments/assets/1d0f6a6e-1666-4664-8f79-7520989f9fbf" />


seq 2 | sed '2i hello'
## OUTPUT


<img width="325" height="123" alt="Screenshot 2025-09-13 134751" src="https://github.com/user-attachments/assets/db04354a-8eeb-4201-8d55-cbf7602b5a1f" />

seq 10 | sed '2,9c hello'
## OUTPUT

<img width="426" height="126" alt="Screenshot 2025-09-13 134823" src="https://github.com/user-attachments/assets/a382cd7c-4701-4b4f-9f45-a7f073d2cf06" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


<img width="476" height="122" alt="Screenshot 2025-09-13 134925" src="https://github.com/user-attachments/assets/5d0af5ba-c6ea-423d-9788-5b7028bccb36" />


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


<img width="382" height="176" alt="Screenshot 2025-09-13 135431" src="https://github.com/user-attachments/assets/d27356f0-56b0-46c6-96b2-dec173decefa" />


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


<img width="358" height="184" alt="Screenshot 2025-09-13 140215" src="https://github.com/user-attachments/assets/ddc87260-e1a4-4e6d-9bbb-1383a3e1216c" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT



<img width="495" height="248" alt="Screenshot 2025-09-13 140331" src="https://github.com/user-attachments/assets/f6930a4c-666c-49fc-8bca-94db9f8c51ee" />


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


<img width="350" height="124" alt="Screenshot 2025-09-13 140730" src="https://github.com/user-attachments/assets/22f0e6b3-768c-45ec-a379-8b8cf5629a3c" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT


<img width="478" height="126" alt="Screenshot 2025-09-13 140809" src="https://github.com/user-attachments/assets/9017a8b5-2042-4725-ac65-acd95d64dcea" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT


<img width="437" height="298" alt="Screenshot 2025-09-13 140851" src="https://github.com/user-attachments/assets/27433b4b-25f0-4dc0-81b5-21022213ffd8" />


mkdir backupdir


<img width="337" height="51" alt="Screenshot 2025-09-13 140955" src="https://github.com/user-attachments/assets/dbfee04d-2086-41f7-9b89-7f8e07962e77" />

mv backup.tar backupdir


<img width="351" height="51" alt="Screenshot 2025-09-13 141002" src="https://github.com/user-attachments/assets/2a63f8b1-c2b1-4c79-a343-bb54568967c9" />


cd backupdir


<img width="275" height="48" alt="Screenshot 2025-09-13 141011" src="https://github.com/user-attachments/assets/e74d35bd-7c53-4c30-b679-ffb9bfe0ecb8" />


tar -tvf backup.tar


## OUTPUT

<img width="809" height="459" alt="Screenshot 2025-09-13 141041" src="https://github.com/user-attachments/assets/03aa6587-89d9-4f50-8e62-721596d5c32a" />


tar -xvf backup.tar
## OUTPUT
<img width="362" height="346" alt="Screenshot 2025-09-13 141115" src="https://github.com/user-attachments/assets/c1c6c80e-6a36-409f-9da4-36e7619407da" />

gzip backup.tar

<img width="408" height="56" alt="Screenshot 2025-09-13 141349" src="https://github.com/user-attachments/assets/e1261b5c-9c4c-47d5-9700-1f7ca166bb62" />

ls .gz
## OUTPUT

<img width="376" height="86" alt="Screenshot 2025-09-13 141357" src="https://github.com/user-attachments/assets/fb4eb5d8-ce6c-483b-9a8f-3f293f561201" />

gunzip backup.tar.gz
## OUTPUT

<img width="370" height="48" alt="Screenshot 2025-09-13 141403" src="https://github.com/user-attachments/assets/f4cefb21-0b13-487f-a50b-0c1403d6c3ea" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="504" height="217" alt="Screenshot 2025-09-13 142110" src="https://github.com/user-attachments/assets/73728f7c-32cd-40f6-9fa3-b502a25ba8ad" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="387" height="125" alt="Screenshot 2025-09-13 142117" src="https://github.com/user-attachments/assets/40fb56cb-7bca-46d5-9ee1-81827cd75e86" />


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

<img width="409" height="55" alt="Screenshot 2025-09-13 142748" src="https://github.com/user-attachments/assets/c16b94f6-d928-481f-9926-6467a16c73c3" />

 <img width="753" height="429" alt="Screenshot 2025-09-13 143013" src="https://github.com/user-attachments/assets/cdf026d3-6fd0-49bf-9fa7-021cfbf317dd" />

ls file1
## OUTPUT

<img width="419" height="84" alt="Screenshot 2025-09-13 143033" src="https://github.com/user-attachments/assets/dc76def5-cd1f-4a27-9de4-fa3b1f1f85fc" />

echo $?
## OUTPUT 

<img width="446" height="79" alt="Screenshot 2025-09-13 143105" src="https://github.com/user-attachments/assets/71cd37c7-9cf8-4726-ad29-6518b6d81045" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 <img width="446" height="79" alt="Screenshot 2025-09-13 143105" src="https://github.com/user-attachments/assets/72451049-43ea-4b7b-a045-b8562a2b740b" />

echo $?
 ## OUTPUT

<img width="446" height="79" alt="Screenshot 2025-09-13 143105" src="https://github.com/user-attachments/assets/7589d12c-cbe5-4a94-b936-8e3825113294" />

 
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
## OUTPUT

<img width="461" height="309" alt="Screenshot 2025-09-13 143153" src="https://github.com/user-attachments/assets/aaaadf57-b6e1-4a69-952e-f84d69c2b4e9" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="437" height="102" alt="Screenshot 2025-09-13 143237" src="https://github.com/user-attachments/assets/353d1a8d-c750-453c-997e-1fc4fb35ee7a" />


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

<img width="520" height="495" alt="Screenshot 2025-09-13 143447" src="https://github.com/user-attachments/assets/1138823e-7c13-4c7b-be36-b66f846c787b" />

<img width="520" height="495" alt="Screenshot 2025-09-13 143447" src="https://github.com/user-attachments/assets/17e80f47-42b7-4018-86ae-f4d227d8ef7b" />

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
## OUTPUT

<img width="434" height="382" alt="Screenshot 2025-09-13 143633" src="https://github.com/user-attachments/assets/d3b014ca-35f7-4e8a-93e7-a36b1ddac809" />


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
## OUTPUT

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

 
 ./funcex.sh 1 2

 
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
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 
 
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


# RESULT:
The Commands are executed successfully.

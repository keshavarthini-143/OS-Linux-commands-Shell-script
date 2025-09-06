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
<img width="368" height="136" alt="1" src="https://github.com/user-attachments/assets/509a02d1-253a-40b7-a756-4a4294144351" />



cat < file2
## OUTPUT

<img width="368" height="136" alt="2" src="https://github.com/user-attachments/assets/c87ecb24-5419-4eed-a927-9885ea7db35b" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="453" height="73" alt="3" src="https://github.com/user-attachments/assets/f02773ec-becf-4c9b-8a7e-6597563fc0f9" />

comm file1 file2
 ## OUTPUT
<img width="443" height="178" alt="4" src="https://github.com/user-attachments/assets/3439b019-3090-4c36-a8b3-7d1a3cb43424" />

 
diff file1 file2
## OUTPUT

<img width="447" height="228" alt="5" src="https://github.com/user-attachments/assets/7b049ca9-972c-4cae-943f-b3a3d379eb25" />

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

<img width="426" height="90" alt="6" src="https://github.com/user-attachments/assets/60a4dfb1-9708-4c6f-b5ff-320d63a78a15" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="490" height="105" alt="7" src="https://github.com/user-attachments/assets/fa957dfa-3638-44b8-b9a3-b6225cadc673" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="490" height="105" alt="8" src="https://github.com/user-attachments/assets/d69be2e8-1715-4c41-a1c5-503865b64550" />


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 ## OUTPUT
<img width="490" height="105" alt="9" src="https://github.com/user-attachments/assets/0aa14810-65e1-4372-8496-1629272033ba" />

 
grep Hello newfile 
## OUTPUT

<img width="499" height="70" alt="10" src="https://github.com/user-attachments/assets/248d5751-6565-4ed1-9622-26beacdd2021" />



grep hello newfile 
## OUTPUT

<img width="499" height="70" alt="11" src="https://github.com/user-attachments/assets/3639286f-a8c0-4fb3-9934-f3517dc158b7" />




grep -v hello newfile 
## OUTPUT
<img width="499" height="70" alt="12" src="https://github.com/user-attachments/assets/4729fee7-c8db-4d8f-82a4-d7cfca28d670" />




cat newfile | grep -i "hello"
## OUTPUT


<img width="561" height="77" alt="13" src="https://github.com/user-attachments/assets/13d1a775-52b5-4624-8147-6f47328ae9a0" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="586" height="66" alt="14" src="https://github.com/user-attachments/assets/eb253a36-df1c-4608-a118-2031e7c41524" />




grep -R ubuntu /etc
## OUTPUT

<img width="1202" height="695" alt="15" src="https://github.com/user-attachments/assets/6c3d1ee8-6f5c-44ff-afd3-cf3b2510cb70" />



grep -w -n world newfile   
## OUTPUT
<img width="616" height="83" alt="16" src="https://github.com/user-attachments/assets/ca37e096-8274-498a-9af8-f41599551b16" />



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
<img width="390" height="143" alt="17" src="https://github.com/user-attachments/assets/632d671b-2a82-4a98-bed7-c49480dfdee4" />


egrep -w 'Hello|hello' newfile 
## OUTPUT

<img width="579" height="79" alt="18" src="https://github.com/user-attachments/assets/001f848d-aab2-4563-9dc7-3d540272acdc" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="579" height="79" alt="19" src="https://github.com/user-attachments/assets/713532dd-3cf1-4632-ba4a-8e73dff5ac04" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="579" height="79" alt="20" src="https://github.com/user-attachments/assets/f988d77c-b828-4513-8792-83d926ade345" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="577" height="64" alt="21" src="https://github.com/user-attachments/assets/ea524c8e-474d-48a6-9cf7-9a03ef144a0c" />



egrep '(world$)' newfile 
## OUTPUT

<img width="577" height="78" alt="22" src="https://github.com/user-attachments/assets/d2540f5b-df0f-43a4-a8d4-a8b43e4deed3" />


egrep '(World$)' newfile 
## OUTPUT

<img width="578" height="54" alt="23" src="https://github.com/user-attachments/assets/e4bf164b-a521-40b2-8a97-be4b3381d63a" />

egrep '((W|w)orld$)' newfile 
## OUTPUT


<img width="575" height="95" alt="24" src="https://github.com/user-attachments/assets/42e4e9d5-0b7e-4d46-8c0f-6838b8209d59" />

egrep '[1-9]' newfile 
## OUTPUT
<img width="574" height="60" alt="25" src="https://github.com/user-attachments/assets/c8cdddbd-dedb-4fed-aee3-7844095f691e" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="574" height="60" alt="26" src="https://github.com/user-attachments/assets/3eb8abd7-f4ac-4418-a7c6-b68f70fc20bb" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="574" height="60" alt="27" src="https://github.com/user-attachments/assets/e79a68c4-2e56-4f8c-9cb6-d7dc7054d8ca" />


egrep l{2} newfile
## OUTPUT

<img width="572" height="77" alt="28" src="https://github.com/user-attachments/assets/7f037c9d-5aaf-4e4a-aabd-a37a2f4388ca" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="575" height="99" alt="29" src="https://github.com/user-attachments/assets/4e6030a7-9bbc-441e-a2a4-67a3304d6978" />


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
<img width="582" height="60" alt="30" src="https://github.com/user-attachments/assets/147a9684-14b2-4a51-8869-b16d4b5ca423" />



sed -n -e '$p' file23
## OUTPUT

<img width="582" height="60" alt="31" src="https://github.com/user-attachments/assets/01785f5f-b3d9-468a-a545-46cdbb86724f" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="571" height="206" alt="32" src="https://github.com/user-attachments/assets/12b6d741-c28d-454d-92dc-c1a1024a477f" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="571" height="206" alt="33" src="https://github.com/user-attachments/assets/6e420c9a-2850-4d55-a4b1-c86044015430" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="571" height="206" alt="34" src="https://github.com/user-attachments/assets/6f5651ea-95b4-418e-ae99-f1cbe1bbd95f" />


sed -n -e '1,5p' file23
## OUTPUT


<img width="572" height="138" alt="35" src="https://github.com/user-attachments/assets/c988eefb-36aa-4ff2-a73c-2d73940bc949" />

sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="572" height="103" alt="36" src="https://github.com/user-attachments/assets/3d925b7c-070f-474f-9b7c-a51de7bb4fde" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


<img width="568" height="76" alt="37" src="https://github.com/user-attachments/assets/70e5e4e9-20ce-4c3e-a3c3-c3a51ac055ae" />

seq 10 
## OUTPUT

<img width="575" height="252" alt="38" src="https://github.com/user-attachments/assets/4d752944-68c2-4a87-8056-f80ceb99ab53" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="568" height="99" alt="39" src="https://github.com/user-attachments/assets/ba78ea95-419f-4afd-aea1-b9cb5b1135bb" />


seq 10 | sed -n '2,~4p'
## OUTPUT


<img width="568" height="99" alt="40" src="https://github.com/user-attachments/assets/e44b1563-cbd9-438f-b85b-6fe1d100666e" />

seq 3 | sed '2a hello'
## OUTPUT
<img width="568" height="121" alt="41" src="https://github.com/user-attachments/assets/03aa5692-cc36-420d-b9bd-af26e2d22ae9" />



seq 2 | sed '2i hello'
## OUTPUT

<img width="569" height="100" alt="42" src="https://github.com/user-attachments/assets/41d70648-b800-44a9-8349-90d2c8b7f703" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="569" height="100" alt="43" src="https://github.com/user-attachments/assets/f561c9ac-a9be-4aa7-8a39-cee931a35e9e" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="569" height="100" alt="44" src="https://github.com/user-attachments/assets/bec87784-1cd5-4052-8f53-457c14562f09" />


sed -n '2,4{s/$/*/;p}' file23

<img width="569" height="100" alt="45" src="https://github.com/user-attachments/assets/d3715565-674c-49b4-aba3-cdd508599610" />

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
<img width="413" height="140" alt="46" src="https://github.com/user-attachments/assets/45ce2bf9-ff43-4954-9739-0f5f677e6bc7" />



cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
```
cat < file22
<img width="414" height="161" alt="47" src="https://github.com/user-attachments/assets/9ab37c2c-1e0a-40f0-8064-60172beb8733" />


uniq file22
## OUTPUT

<img width="411" height="147" alt="48" src="https://github.com/user-attachments/assets/10e280ba-73d7-4aad-8736-e84e1d583041" />




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

 <img width="632" height="209" alt="49" src="https://github.com/user-attachments/assets/0f26681f-42c0-4847-9189-782889ac02e7" />


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
<img width="467" height="100" alt="50" src="https://github.com/user-attachments/assets/f0630dba-b598-466e-9e3d-bb3e1dba2723" />

cat urllist.txt | tr -d ' '
 ## OUTPUT

<img width="467" height="100" alt="51" src="https://github.com/user-attachments/assets/51aa8941-61a9-4ff1-af2b-4fdd95bb5703" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="662" height="107" alt="52" src="https://github.com/user-attachments/assets/6b5c25d4-7cde-42ce-80b9-ee012c1faa2b" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="524" height="272" alt="53" src="https://github.com/user-attachments/assets/31ff57c6-f815-43df-a14a-aa1168041cd0" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="744" height="274" alt="54" src="https://github.com/user-attachments/assets/505f025a-9b55-4184-b77f-7a932722c3dd" />


tar -xvf backup.tar
## OUTPUT
<img width="578" height="270" alt="55" src="https://github.com/user-attachments/assets/a86b159c-8f2a-444e-afa7-2293123ea027" />


gzip backup.tar

ls .gz
## OUTPUT
 <img width="580" height="63" alt="56" src="https://github.com/user-attachments/assets/d471c8ba-39ef-4a9a-b22d-04c51fcb25d2" />

gunzip backup.tar.gz
ls
## OUTPUT
<img width="903" height="80" alt="57" src="https://github.com/user-attachments/assets/4fa8d26b-bee5-43e0-96b2-b6012dae39b8" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="889" height="134" alt="58" src="https://github.com/user-attachments/assets/01747174-2798-4bcb-aac0-cf7e64a8e6bf" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="450" height="106" alt="59" src="https://github.com/user-attachments/assets/489085e2-e93b-4064-88a1-22bbab705d4b" />


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
## OUTPUT

 <img width="436" height="278" alt="60" src="https://github.com/user-attachments/assets/ddfde304-9f91-46dd-95c1-6856f87fd256" />
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT

<img width="650" height="361" alt="61" src="https://github.com/user-attachments/assets/d391054a-eddc-4305-8515-4a6fa1457543" />

 
ls file1
## OUTPUT
<img width="371" height="55" alt="62" src="https://github.com/user-attachments/assets/7b13441a-9e9d-4a16-9bae-cd8ab509d452" />

echo $?
## OUTPUT 
<img width="371" height="55" alt="63" src="https://github.com/user-attachments/assets/d681c2c2-d4a3-411d-93a2-51c518ec5d63" />



./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="404" height="94" alt="64" src="https://github.com/user-attachments/assets/9295237a-9c9c-43e1-8079-264e995b3e6d" />

abcd
 
echo $?
 ## OUTPUT
<img width="395" height="51" alt="65" src="https://github.com/user-attachments/assets/ffc7341d-f333-4dff-a087-8b764f520f4e" />


 
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
<img width="420" height="236" alt="66" src="https://github.com/user-attachments/assets/c152de37-c49f-44ce-96c1-11898a406808" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="637" height="96" alt="67" src="https://github.com/user-attachments/assets/6782ff08-5233-4efa-8842-8719c13272cd" />

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
## OUTPUT
<img width="614" height="184" alt="68" src="https://github.com/user-attachments/assets/a6543c46-c973-417b-a0ce-6e038202498b" />



./psswdperm.sh
## OUTPUT

<img width="454" height="47" alt="69" src="https://github.com/user-attachments/assets/faac0742-994e-4857-b166-da8b2b822af1" />


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

## OUTPUT

<img width="452" height="404" alt="70" src="https://github.com/user-attachments/assets/da164d76-c15b-43e3-8a5e-4fff6a1c7fde" />


./ifnested.sh 
## OUTPUT

<img width="461" height="57" alt="71" src="https://github.com/user-attachments/assets/5d4a3770-412b-4691-ba94-6e969ac47fb9" />


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
## OUTPUT

<img width="457" height="319" alt="72" src="https://github.com/user-attachments/assets/081fe00c-54d2-48be-96ed-cea0c1371b84" />


$ chmod 755 iftest.sh
 
$ ./iftest.sh 
## OUTPUT

<img width="612" height="125" alt="73" src="https://github.com/user-attachments/assets/50a9d470-50b2-4304-b29c-24252901e960" />


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
## OUTPUT

<img width="507" height="407" alt="74" src="https://github.com/user-attachments/assets/7558647f-53ba-41cf-9be3-17c2c22aa6fd" />


$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
## OUTPUT

<img width="636" height="140" alt="75" src="https://github.com/user-attachments/assets/4fe763ba-798b-4321-b8d7-576acb55c25e" />


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

<img width="637" height="99" alt="76" src="https://github.com/user-attachments/assets/b64fdb18-1336-4ee8-b712-75c6350d07ef" />


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

<img width="637" height="99" alt="77" src="https://github.com/user-attachments/assets/fc698478-20fd-45e5-b8e2-d91b4413f832" />


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

## OUTPUT


<img width="507" height="81" alt="78" src="https://github.com/user-attachments/assets/1994822b-fc45-46ce-a220-0a065fd2cf5f" />

 
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

## OUTPUT

<img width="642" height="295" alt="79" src="https://github.com/user-attachments/assets/9c4bf3af-16c2-47cf-bedc-61747d15e8ed" />

 
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
## OUTPUT

<img width="550" height="165" alt="80" src="https://github.com/user-attachments/assets/efbb00e8-2c3b-4fd9-bc46-8c3577c833e4" />

 
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

## OUTPUT 

<img width="631" height="233" alt="81" src="https://github.com/user-attachments/assets/21dc23d0-f3d2-4da4-a77c-5a9fc5eaa558" />


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

## OUTPUT

<img width="635" height="168" alt="82" src="https://github.com/user-attachments/assets/ab981f21-f113-4e54-a807-9c14f7b2c09f" />


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

## OUTPUT

<img width="685" height="115" alt="83" src="https://github.com/user-attachments/assets/690b4595-073a-49b0-918c-3e0b28f0d443" />


 
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

## OUTPUT

<img width="683" height="224" alt="84" src="https://github.com/user-attachments/assets/4a058a9d-8142-4747-b403-58baedcf3648" />


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

<img width="512" height="77" alt="85" src="https://github.com/user-attachments/assets/21e1e6eb-b3c4-45dd-a6b5-497b970d8a75" />


cat > forinfile.sh 
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

<img width="389" height="173" alt="86" src="https://github.com/user-attachments/assets/94b69753-7d41-483b-90cb-d370f2649be0" />


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

<img width="635" height="184" alt="87" src="https://github.com/user-attachments/assets/4ac762aa-6993-44f1-963e-0f46032d56e1" />


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
<img width="635" height="184" alt="88" src="https://github.com/user-attachments/assets/802819ff-c354-48d0-92e3-2b74354dd4ae" />

cat > fornested1.sh 
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
<img width="648" height="338" alt="89" src="https://github.com/user-attachments/assets/f4856f3a-faf9-4f0a-a17e-aeccd0a3c79c" />

 
cat > forbreak.sh 
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

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
## OUTPUT

<img width="652" height="139" alt="90" src="https://github.com/user-attachments/assets/d2369c6f-f303-4e61-88ec-86d73164e7a8" />

 
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
 <img width="677" height="330" alt="91" src="https://github.com/user-attachments/assets/fa9a8364-ff85-4754-9143-3b1f4f171995" />

cat > exread.sh 
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
<img width="621" height="130" alt="92" src="https://github.com/user-attachments/assets/435085ec-77b7-4605-994d-cba29545347a" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 
$ ./exread1.sh 

## OUTPUT




 
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

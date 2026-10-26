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
<img width="630" height="157" alt="cat _ file1" src="https://github.com/user-attachments/assets/c0481f8e-cdcc-4a96-8122-a14591e6d868" />





cat < file2
## OUTPUT
<img width="588" height="177" alt="cat _ file2" src="https://github.com/user-attachments/assets/2fbee88a-ff40-4119-84f2-530977aec887" />



# Comparing Files
cmp file1 file2
## OUTPUT
<img width="592" height="78" alt="cmp file1 file2" src="https://github.com/user-attachments/assets/5624c086-2d8e-47f6-9d4d-6fa9e32340e3" />


 
comm file1 file2
 ## OUTPUT
<img width="620" height="233" alt="comm file1 file2" src="https://github.com/user-attachments/assets/30047d7f-a90f-4495-8514-75e8f0dded29" />

 
diff file1 file2
## OUTPUT

<img width="595" height="279" alt="diff file1 file2" src="https://github.com/user-attachments/assets/b7e9f7ed-62c4-4888-9f18-395539b12195" />


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

<img width="642" height="95" alt="cut -c1-3 file11" src="https://github.com/user-attachments/assets/1196de37-7366-4bba-ab6c-baffc056f7d0" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="616" height="134" alt="cut -d ___ -f 1 file22" src="https://github.com/user-attachments/assets/8415c3c8-6d15-4268-ae3f-30b82389f0c8" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="615" height="130" alt="cut -d ___ -f 2 file22" src="https://github.com/user-attachments/assets/77a712e0-3ac4-4588-b9c9-47b10a8898db" />


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

<img width="578" height="73" alt="grep Hello newfile" src="https://github.com/user-attachments/assets/146c12ba-151a-49a9-af7e-15aea0620d99" />



grep hello newfile 
## OUTPUT

<img width="571" height="77" alt="grep hello newfile" src="https://github.com/user-attachments/assets/cad13476-2b23-48dc-9106-52346c129d4c" />




grep -v hello newfile 
## OUTPUT

<img width="576" height="80" alt="grep -v hello newfile" src="https://github.com/user-attachments/assets/72ff8ee2-56e6-480b-9fd1-08cf7873ff34" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="579" height="101" alt="cat newfile _ grep -i _hello_" src="https://github.com/user-attachments/assets/727d540d-ada8-4ae2-a67e-ef3536ccf9c9" />




cat newfile | grep -i -c "hello"
## OUTPUT


<img width="591" height="82" alt="cat newfile _ grep -i -c _hello_" src="https://github.com/user-attachments/assets/7c369229-f6b6-4b2f-b704-dec32767eea2" />



grep -R ubuntu /etc
## OUTPUT



<img width="1277" height="818" alt="grep R ubuntu " src="https://github.com/user-attachments/assets/6e730d9f-0997-4f01-a4b4-5f99f149775d" />

grep -w -n world newfile   
## OUTPUT

<img width="649" height="99" alt="grep -w -n world newfile" src="https://github.com/user-attachments/assets/6203b3e2-af6a-45af-ab22-2c50aa39bf20" />


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


<img width="592" height="99" alt="egrep -w &#39;Hello_hello&#39; newfile" src="https://github.com/user-attachments/assets/823dab55-8e89-4867-b98f-297dcfad3800" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="610" height="94" alt="egrep -w &#39;(H_h)ello&#39; newfile" src="https://github.com/user-attachments/assets/521b3da0-fed0-4d79-880f-e619af607253" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="610" height="106" alt="egrep -w &#39;(H_h)ell a-z &#39; newfile" src="https://github.com/user-attachments/assets/b329a685-3102-4574-b505-d8cb8d5bc1c6" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="608" height="69" alt="egrep &#39;(^hello)&#39; newfile" src="https://github.com/user-attachments/assets/fb98e0a8-2c2e-43a2-a7ce-e4f121a377e0" />



egrep '(world$)' newfile 
## OUTPUT

<img width="572" height="100" alt="egrep &#39;(world$)&#39; newfile" src="https://github.com/user-attachments/assets/b90696f0-19aa-47e5-b951-ff13b7b09b4d" />



egrep '(World$)' newfile 
## OUTPUT

<img width="605" height="75" alt="egrep &#39;(World$)&#39; newfile" src="https://github.com/user-attachments/assets/a9f62f98-e460-4e25-8b6f-a3c0554cd5a7" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="603" height="124" alt="egrep &#39;((W_w)orld$)&#39; newfile" src="https://github.com/user-attachments/assets/b15350ac-7065-41ad-854a-5866c3c1d2b9" />



egrep '[1-9]' newfile 
## OUTPUT


<img width="641" height="81" alt="egrep &#39; 1-9 &#39; newfile" src="https://github.com/user-attachments/assets/6dc7a991-87eb-4d41-a142-eddcb5712b86" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="627" height="77" alt="egrep &#39;Linux _world&#39; newfile" src="https://github.com/user-attachments/assets/cbc75b9c-e155-453d-b344-3a2b4b93133b" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="617" height="76" alt="egrep &#39;Linux _World&#39; newfile" src="https://github.com/user-attachments/assets/265f45a7-4688-49a7-a3ab-dcc3b8692d9c" />


egrep l{2} newfile
## OUTPUT


<img width="611" height="102" alt="egrep l{2} newfile" src="https://github.com/user-attachments/assets/d0aaec81-05b4-4e3f-84d5-6df7feac1e7a" />


egrep 's{1,2}' newfile
## OUTPUT 


<img width="637" height="127" alt="egrep &#39;s{1,2}&#39; newfile" src="https://github.com/user-attachments/assets/f03cd8f8-9058-44fa-a151-367d6dbdbf07" />

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

<img width="583" height="75" alt="sed -n -e &#39;3p&#39; file23" src="https://github.com/user-attachments/assets/c9153a5b-5297-463b-a2c1-c0723b9c5429" />



sed -n -e '$p' file23
## OUTPUT

<img width="568" height="70" alt="sed -n -e &#39;$p&#39; file23" src="https://github.com/user-attachments/assets/9e00ea4d-4b88-462a-88b1-719e4d036857" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="568" height="70" alt="sed -n -e &#39;$p&#39; file23" src="https://github.com/user-attachments/assets/e7a1a9bf-3d5c-4a1f-808e-6b4a8bb106b6" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="607" height="247" alt="sed -e &#39;s Ram Sita &#39; file23" src="https://github.com/user-attachments/assets/e3853f89-3992-4c3b-80d7-4609f82fc584" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT


<img width="621" height="250" alt="sed &#39; tom s 5000 6000 &#39; file23" src="https://github.com/user-attachments/assets/f45d4087-dc52-4b39-811b-6303f35c109d" />


sed -n -e '1,5p' file23
## OUTPUT


<img width="597" height="179" alt="sed -n -e &#39;1,5p&#39; file23" src="https://github.com/user-attachments/assets/0cdaffb2-ce99-4d60-a19b-e5ea495b4eb4" />


sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="612" height="126" alt="sed -n -e &#39;2, Joe p&#39; file23" src="https://github.com/user-attachments/assets/0f2831a5-7d5f-4504-a611-79890b5fd0f3" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


<img width="582" height="96" alt="sed -n -e &#39; tom , Joe p&#39; file23" src="https://github.com/user-attachments/assets/a1ca2a78-78f3-430a-91ff-b606a3ca1834" />


seq 10 
## OUTPUT

<img width="575" height="294" alt="seq 10" src="https://github.com/user-attachments/assets/97f078bf-69a1-4b6b-ba22-16c00668406d" />



seq 10 | sed -n '4,6p'
## OUTPUT


<img width="570" height="119" alt="seq 10 _ sed -n &#39;4,6p&#39;" src="https://github.com/user-attachments/assets/1b265e00-abc1-47cf-820e-5427a04f66bd" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="564" height="120" alt="seq 10 _ sed -n &#39;2,~4p&#39;" src="https://github.com/user-attachments/assets/c6bfe53f-673a-4ad7-82ef-5fd2d4f1dc28" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="591" height="150" alt="seq 3 _ sed &#39;2a hello&#39;" src="https://github.com/user-attachments/assets/80e3c236-2b78-4ae8-a15c-74e39ae2a48a" />



seq 2 | sed '2i hello'
## OUTPUT


<img width="569" height="120" alt="seq 2 _ sed &#39;2i hello&#39;" src="https://github.com/user-attachments/assets/2b820f85-9ae2-4184-bf3f-e5b0de674310" />

seq 10 | sed '2,9c hello'
## OUTPUT


<img width="574" height="121" alt="seq 10 _ sed &#39;2,9c hello&#39;" src="https://github.com/user-attachments/assets/d1b61b7a-2d88-41d1-8b4b-5ef23d9fc873" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


<img width="578" height="128" alt="sed -n &#39;2,4{s $ __" src="https://github.com/user-attachments/assets/005374ae-e620-4800-8fef-5d5bfa208bf0" />

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

<img width="332" height="181" alt="sort file21" src="https://github.com/user-attachments/assets/b34d6ab6-bd23-4aeb-981f-872da68a88b8" />


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


<img width="346" height="179" alt="uniq file22" src="https://github.com/user-attachments/assets/85a66db8-713e-4f5d-b4d5-afdd70b9c765" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="455" height="201" alt="cat file23 _ tr  _lower_   _upper_" src="https://github.com/user-attachments/assets/c4858b04-682f-4ef4-a851-ba4b2a79acce" />

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


<img width="381" height="125" alt="cat urllist txt _ tr -d &#39; &#39;" src="https://github.com/user-attachments/assets/8fd73515-1179-4d2c-92fc-98156bc46943" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT


<img width="502" height="126" alt="cat urllist txt _ tr -d &#39; &#39; _ tr -s &#39; &#39;" src="https://github.com/user-attachments/assets/21bd16b5-19b6-4d7c-8aaa-d26aa1f4bafd" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT


<img width="765" height="855" alt="tar -cvf backup tar _" src="https://github.com/user-attachments/assets/19c188f9-fdc0-4cae-b106-e926758fd7dd" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


<img width="1326" height="871" alt="tar -tvf backup tar" src="https://github.com/user-attachments/assets/b969796a-899a-4748-bb45-0eb702e4575e" />

tar -xvf backup.tar
## OUTPUT

<img width="787" height="850" alt="tar -xvf backup tar" src="https://github.com/user-attachments/assets/93257218-59da-419a-be05-41dfe70cab17" />

gzip backup.tar

ls .gz
## OUTPUT

 <img width="387" height="71" alt="ls  gz" src="https://github.com/user-attachments/assets/cb8b0048-8f0e-4b09-9b79-0cded7c52ae4" />

gunzip backup.tar.gz
## OUTPUT

<img width="1781" height="285" alt="gunzip backup tar gz" src="https://github.com/user-attachments/assets/e4e1d2aa-52db-45ed-8bf2-1166d0ddbaf7" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="605" height="79" alt="_my-script sh" src="https://github.com/user-attachments/assets/cf74b24c-84b5-4b4c-8adc-f1394c2d0e3e" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="417" height="120" alt="cat herecheck txt" src="https://github.com/user-attachments/assets/49f2d47e-c42b-4b19-b8d7-26509c3d49c8" />


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

<img width="677" height="391" alt="_scriptest sh" src="https://github.com/user-attachments/assets/b9f168db-564d-4f4b-bc37-b39c4f34f92c" />

 
ls file1
## OUTPUT

<img width="343" height="75" alt="ls file1" src="https://github.com/user-attachments/assets/9cbcf30a-c45d-4c04-85ea-8928e3fcd693" />

echo $?
## OUTPUT 

<img width="262" height="84" alt="echo1" src="https://github.com/user-attachments/assets/470cc945-f6ff-481a-826a-af8bc49dcd95" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

 <img width="523" height="154" alt="echo2" src="https://github.com/user-attachments/assets/ed7d3499-15f3-47a6-81c6-9e89d96480fa" />

abcd
 
echo $?
 ## OUTPUT

<img width="377" height="152" alt="echo3" src="https://github.com/user-attachments/assets/b2066cb9-7206-4c42-b5eb-e3e4ccc28ece" />


 
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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="622" height="75" alt="_strcomp sh" src="https://github.com/user-attachments/assets/62c1da9d-2479-41e2-a4fd-3e0a955afaec" />


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

<img width="612" height="86" alt="_psswdperm sh" src="https://github.com/user-attachments/assets/d00ad3fd-dcb3-4390-bbf7-44d52314f55d" />

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

<img width="612" height="145" alt="_ifnested sh" src="https://github.com/user-attachments/assets/9cc7a9fe-71f6-4e05-a06b-ee04f5b61f69" />



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
<img width="592" height="108" alt="_iftest sh " src="https://github.com/user-attachments/assets/1946561d-a3b6-4e4a-a438-4c6b62f260e3" />


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

<img width="612" height="145" alt="_ifnested sh" src="https://github.com/user-attachments/assets/2aa9fe84-bf15-4048-8464-6e6009110d3e" />

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

<img width="597" height="88" alt="_elifcheck sh " src="https://github.com/user-attachments/assets/ce69d093-fd56-4546-802e-63e014576d91" />




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

<img width="611" height="91" alt="_ifcompound sh " src="https://github.com/user-attachments/assets/c19740a8-6ae3-4ba0-b8cb-7ebd185064c4" />

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

 ##OUTPUT
 <img width="437" height="80" alt="_  casecheck sh" src="https://github.com/user-attachments/assets/3ce0933d-70d7-4cc7-b883-81a4f5e61235" />

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
 ##OUTPUT
 <img width="626" height="311" alt="_whiletest sh" src="https://github.com/user-attachments/assets/3158e894-89df-4d5f-a91e-91bb4ae790c4" />

 
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
 
 ##OUTPUT
 <img width="602" height="162" alt="_untiltest sh" src="https://github.com/user-attachments/assets/75ac8a4f-388a-4da1-a46e-0c2978e74221" />

 
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
##OUTPUT
<img width="655" height="218" alt="_forin1 sh" src="https://github.com/user-attachments/assets/0426f328-3292-42e6-a64b-a7b74b57fb4f" />

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

<img width="315" height="172" alt="_forctype1 sh" src="https://github.com/user-attachments/assets/7bfd7611-698b-42bd-b260-19db70ddb252" />

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


<img width="650" height="223" alt="_firinfile sh" src="https://github.com/user-attachments/assets/53c1408b-a059-4c1e-b0da-7aa5388241a9" />

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

<img width="318" height="171" alt="_forctype sh" src="https://github.com/user-attachments/assets/e271c10d-d53c-45f9-8f43-b528c37aec8f" />


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

<img width="315" height="172" alt="_forctype1 sh" src="https://github.com/user-attachments/assets/33a39dfa-7cbe-46b0-8c87-f9f343390219" />

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


 <img width="277" height="131" alt="_forbreak sh" src="https://github.com/user-attachments/assets/d5f1b3e8-f156-40fd-b011-188ea34a6d50" />

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


$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
## OUTPUT
 <img width="252" height="359" alt="_fornested1 sh" src="https://github.com/user-attachments/assets/aad75570-385f-43ad-ade1-1e1badad1f42" />

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

 <img width="307" height="178" alt="_forcontinue sh" src="https://github.com/user-attachments/assets/60176074-fc48-4294-b7c6-ba391792bfa0" />

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

<img width="400" height="109" alt="_exread sh" src="https://github.com/user-attachments/assets/a5595cba-1c15-4b3e-abb4-8259a24a1952" />


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

 <img width="403" height="106" alt="_exread1 sh" src="https://github.com/user-attachments/assets/2eeba71e-81f6-4138-b96e-88cd487b310f" />

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

 ./funcex.sh 

 
 ./funcex.sh 1 2

## OUTPUT 
<img width="321" height="128" alt="_argshift1 sh 1 2 3" src="https://github.com/user-attachments/assets/7de64969-05a1-4849-bdf0-0be1dafa1d1f" />

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
<img width="327" height="131" alt="_argshift sh 1 2 3" src="https://github.com/user-attachments/assets/cb0c516f-ce88-468f-9972-20c2b4f4f6b3" />

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
$ ./argshift.sh 1 2 3
## OUTPUT

 <img width="321" height="128" alt="_argshift1 sh 1 2 3" src="https://github.com/user-attachments/assets/2a799f6b-b56a-4339-b000-abe2d8d19989" />

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
 <img width="321" height="128" alt="_argshift1 sh 1 2 3" src="https://github.com/user-attachments/assets/a3467f15-7203-446e-b266-ffbc2cff36f9" />

 
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

 <img width="333" height="376" alt="awk -f nc awk data dat" src="https://github.com/user-attachments/assets/3be6edb7-da94-4a7c-981d-0cea0340bafe" />

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

<img width="386" height="125" alt="_palindrome sh" src="https://github.com/user-attachments/assets/5e1aadb8-a3c7-45dd-bc01-b50ab39c12ca" />


# RESULT:
The Commands are executed successfully.

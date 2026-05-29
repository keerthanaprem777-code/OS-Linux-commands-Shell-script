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
<img width="210" height="101" alt="Screenshot 2026-05-29 185456" src="https://github.com/user-attachments/assets/cf7b5d59-1352-4dcb-ac0b-6fe2bac2e1ac" />

cat < file2
## OUTPUT
<img width="204" height="109" alt="Screenshot 2026-05-29 185503" src="https://github.com/user-attachments/assets/ef6bbf83-57fb-4de1-ba4e-b78381675c47" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="281" height="60" alt="Screenshot 2026-05-29 185511" src="https://github.com/user-attachments/assets/8b735e15-2d2e-48cf-ae3a-65a7ded72274" />

comm file1 file2
 ## OUTPUT
<img width="267" height="140" alt="Screenshot 2026-05-29 185528" src="https://github.com/user-attachments/assets/0541b43a-522b-4c90-9653-540b020c4b59" />
 
diff file1 file2
## OUTPUT
<img width="273" height="186" alt="Screenshot 2026-05-29 185538" src="https://github.com/user-attachments/assets/6a0be072-a341-4b61-8191-907f94304524" />

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
<img width="224" height="73" alt="Screenshot 2026-05-29 185554" src="https://github.com/user-attachments/assets/d6fda541-37d4-43c9-b2b6-7a0b8d419d75" />

cut -d "|" -f 1 file22
## OUTPUT
<img width="249" height="85" alt="Screenshot 2026-05-29 185612" src="https://github.com/user-attachments/assets/028e6603-a4fb-4136-a204-8e70ad84dbc2" />

cut -d "|" -f 2 file22
## OUTPUT
<img width="249" height="85" alt="Screenshot 2026-05-29 185612" src="https://github.com/user-attachments/assets/1fa80394-707b-4de0-bc51-24ba6ea0b75c" />

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
<img width="226" height="44" alt="Screenshot 2026-05-29 185637" src="https://github.com/user-attachments/assets/859bc069-345c-47f9-a3c9-d705e4599324" />

grep hello newfile 
## OUTPUT
<img width="226" height="44" alt="Screenshot 2026-05-29 185637" src="https://github.com/user-attachments/assets/b70d8ddf-f759-4f4d-9aa3-c95ca9aef490" />

grep -v hello newfile 
## OUTPUT
<img width="288" height="59" alt="Screenshot 2026-05-29 185653" src="https://github.com/user-attachments/assets/924b9f16-1dad-4c22-a150-513dac713820" />

cat newfile | grep -i "hello"
## OUTPUT
<img width="296" height="65" alt="Screenshot 2026-05-29 185701" src="https://github.com/user-attachments/assets/0370db91-48f7-4ae7-b0d5-a0382c71b0d0" />

cat newfile | grep -i -c "hello"
## OUTPUT
<img width="319" height="52" alt="Screenshot 2026-05-29 185717" src="https://github.com/user-attachments/assets/040d2c40-4167-4bd2-83eb-94d897ea9f14" />

grep -R ubuntu /etc
## OUTPUT
<img width="428" height="133" alt="Screenshot 2026-05-29 185730" src="https://github.com/user-attachments/assets/4cf618d1-bb17-4f09-a4ce-b7770c94ff10" />
<img width="436" height="371" alt="Screenshot 2026-05-29 185752" src="https://github.com/user-attachments/assets/c1fa01da-9b35-437a-9cae-1506c8050470" />

grep -w -n world newfile   
## OUTPUT
<img width="284" height="79" alt="Screenshot 2026-05-29 185808" src="https://github.com/user-attachments/assets/95a89e7f-ea9d-402f-b701-acdd16391855" />

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
<img width="314" height="69" alt="Screenshot 2026-05-29 185828" src="https://github.com/user-attachments/assets/cc363bee-2f4b-437e-be0b-60761f267ec5" />

egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="275" height="63" alt="Screenshot 2026-05-29 185837" src="https://github.com/user-attachments/assets/25a088a6-a4e7-4349-bb26-83db2f1ad050" />

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="273" height="79" alt="Screenshot 2026-05-29 185928" src="https://github.com/user-attachments/assets/2579cac5-5175-4db9-957e-9f4140caef78" />

egrep '(^hello)' newfile 
## OUTPUT
<img width="254" height="51" alt="Screenshot 2026-05-29 185935" src="https://github.com/user-attachments/assets/2538046d-f186-471b-8265-875a7133c709" />

egrep '(world$)' newfile 
## OUTPUT
<img width="260" height="65" alt="Screenshot 2026-05-29 185942" src="https://github.com/user-attachments/assets/8435c800-510a-45de-a1a1-4ddf523e53c9" />

egrep '(World$)' newfile 
## OUTPUT
<img width="275" height="37" alt="Screenshot 2026-05-29 190000" src="https://github.com/user-attachments/assets/678bf6be-4bac-438a-8c95-35257599f212" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="260" height="80" alt="Screenshot 2026-05-29 190019" src="https://github.com/user-attachments/assets/2b0504ba-8bd2-4053-9c53-5234ede3a0af" />

egrep '[1-9]' newfile 
## OUTPUT
<img width="315" height="58" alt="Screenshot 2026-05-29 190027" src="https://github.com/user-attachments/assets/e4e69c66-0afc-4b43-8c96-efe6dcd84564" />

egrep 'Linux.*world' newfile 
## OUTPUT
<img width="297" height="57" alt="Screenshot 2026-05-29 190036" src="https://github.com/user-attachments/assets/ac064055-4d95-4b9d-947d-7a55908ccf05" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="297" height="57" alt="Screenshot 2026-05-29 190036" src="https://github.com/user-attachments/assets/681c14e7-bc6b-4552-8729-85427e76c0b1" />

egrep l{2} newfile
## OUTPUT
<img width="206" height="72" alt="Screenshot 2026-05-29 190123" src="https://github.com/user-attachments/assets/65d08e4b-7c88-41aa-ada7-84850f8b8aa7" />

egrep 's{1,2}' newfile
## OUTPUT 
<img width="231" height="85" alt="Screenshot 2026-05-29 190136" src="https://github.com/user-attachments/assets/5384af28-90b8-46b0-9f4f-f932d3039407" />

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
<img width="261" height="54" alt="Screenshot 2026-05-29 190146" src="https://github.com/user-attachments/assets/58e3da08-45c0-44ee-b194-d58a782bca8b" />

sed -n -e '$p' file23
## OUTPUT
<img width="209" height="52" alt="Screenshot 2026-05-29 190204" src="https://github.com/user-attachments/assets/4eb323f5-e7ee-47bb-b054-b05fd4466cab" />

sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="295" height="162" alt="Screenshot 2026-05-29 190210" src="https://github.com/user-attachments/assets/7912181e-5bb8-4567-9f8f-b6d4afda4352" />

sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="272" height="155" alt="Screenshot 2026-05-29 190226" src="https://github.com/user-attachments/assets/66c7d524-94b7-412d-9b11-a53c6b1b3244" />

sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="255" height="178" alt="Screenshot 2026-05-29 190235" src="https://github.com/user-attachments/assets/14ad5bbe-2444-424e-8351-5edb62b07216" />

sed -n -e '1,5p' file23
## OUTPUT
<img width="280" height="113" alt="Screenshot 2026-05-29 190249" src="https://github.com/user-attachments/assets/cc55d761-1f08-485d-9b57-860589de56ce" />

sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="288" height="76" alt="Screenshot 2026-05-29 190256" src="https://github.com/user-attachments/assets/0b88239d-87ba-4231-98a0-d6ed34f79d61" />

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="282" height="70" alt="Screenshot 2026-05-29 190301" src="https://github.com/user-attachments/assets/62286aa2-f223-43cc-9099-23c38c10a456" />

seq 10 
## OUTPUT
<img width="171" height="182" alt="Screenshot 2026-05-29 190314" src="https://github.com/user-attachments/assets/e926e4df-e6c7-4fba-944c-95eaa14def96" />

seq 10 | sed -n '4,6p'
## OUTPUT
<img width="204" height="82" alt="Screenshot 2026-05-29 190320" src="https://github.com/user-attachments/assets/ce318954-6f83-465e-b4dc-fa4d2c4efdd9" />

seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="205" height="85" alt="Screenshot 2026-05-29 190336" src="https://github.com/user-attachments/assets/e50d98a7-3960-4b26-a06f-e7c73dcc0ecc" />

seq 3 | sed '2a hello'
## OUTPUT
<img width="192" height="101" alt="Screenshot 2026-05-29 190342" src="https://github.com/user-attachments/assets/e49f8325-f9c3-4069-a780-328b5eb3f95a" />

seq 2 | sed '2i hello'
## OUTPUT
<img width="215" height="82" alt="Screenshot 2026-05-29 190349" src="https://github.com/user-attachments/assets/17bcabc1-2b5d-43bf-b8ee-1fb60fb974bf" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="245" height="80" alt="Screenshot 2026-05-29 190429" src="https://github.com/user-attachments/assets/0c108e1c-3226-4c16-838f-70617b21f237" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="278" height="88" alt="Screenshot 2026-05-29 190446" src="https://github.com/user-attachments/assets/02b7e153-9113-48d8-a02d-83495bc70aaa" />

sed -n '2,4{s/$/*/;p}' file23
<img width="256" height="86" alt="Screenshot 2026-05-29 190457" src="https://github.com/user-attachments/assets/a42bfb6c-9ffd-4626-b604-31241470bcc4" />

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
<img width="217" height="114" alt="Screenshot 2026-05-29 190512" src="https://github.com/user-attachments/assets/db9e30c6-58d6-4832-95ac-7ab246f521d5" />

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
<img width="221" height="117" alt="Screenshot 2026-05-29 190530" src="https://github.com/user-attachments/assets/dacb31f7-1037-4383-9f62-b023e40b490f" />

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="335" height="169" alt="Screenshot 2026-05-29 190538" src="https://github.com/user-attachments/assets/b2638dc8-217c-4908-8d5d-90b418b5a8a3" />

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
<img width="264" height="88" alt="Screenshot 2026-05-29 202640" src="https://github.com/user-attachments/assets/62303d18-1133-4019-b01c-ba73f5d56fc7" />

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="308" height="91" alt="Screenshot 2026-05-29 202655" src="https://github.com/user-attachments/assets/fa9ac7db-f062-466a-aeb6-70366b3892e9" />

#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="240" height="170" alt="Screenshot 2026-05-29 202705" src="https://github.com/user-attachments/assets/225491e1-af82-45f5-8f0d-8b50cea011be" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="409" height="173" alt="Screenshot 2026-05-29 202730" src="https://github.com/user-attachments/assets/3668fa35-6eeb-43cb-a8f4-a6bc3dc4ba5f" />

tar -xvf backup.tar
## OUTPUT
<img width="246" height="177" alt="Screenshot 2026-05-29 202741" src="https://github.com/user-attachments/assets/443c0738-6a74-46a9-bc11-317123f84031" />

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
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
<img width="383" height="128" alt="Screenshot 2026-05-29 184148" src="https://github.com/user-attachments/assets/09de7ee9-1bc4-4816-8398-0735ec5e70b8" />

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
<img width="240" height="220" alt="Screenshot 2026-05-29 203133" src="https://github.com/user-attachments/assets/bcc6bf1c-043e-41e4-84ee-8357e8f98deb" />

ls file1
## OUTPUT
<img width="228" height="60" alt="Screenshot 2026-05-29 203902" src="https://github.com/user-attachments/assets/744a322e-57a3-4f3a-b6ee-65a7533e8e4f" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
<img width="233" height="60" alt="Screenshot 2026-05-29 203924" src="https://github.com/user-attachments/assets/09c2e97f-d9d5-41b9-b4d3-2b76d817760b" />
 
echo $?
## OUTPUT 
 <img width="260" height="70" alt="Screenshot 2026-05-29 203937" src="https://github.com/user-attachments/assets/3eee75ae-9000-4b9e-83c6-209c81e28689" />

abcd
 
echo $?
 ## OUTPUT
<img width="257" height="61" alt="Screenshot 2026-05-29 203951" src="https://github.com/user-attachments/assets/82abaa8a-5a7d-4d80-967e-3e2961d28774" />

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
<img width="243" height="186" alt="Screenshot 2026-05-29 204221" src="https://github.com/user-attachments/assets/b5949eeb-1d95-455d-8081-c6bcdc0b879f" />

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="243" height="186" alt="Screenshot 2026-05-29 204221" src="https://github.com/user-attachments/assets/723d9c18-08f4-470c-8547-42b0a092818d" />

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
<img width="411" height="164" alt="Screenshot 2026-05-29 204327" src="https://github.com/user-attachments/assets/7031481b-db2b-4a89-9c85-d1102a3368e3" />

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
<img width="343" height="304" alt="Screenshot 2026-05-29 204431" src="https://github.com/user-attachments/assets/ac1fcd06-450a-48fa-9b34-e94d86d6fa35" />

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
<img width="318" height="322" alt="Screenshot 2026-05-29 204503" src="https://github.com/user-attachments/assets/91091d83-2fc7-4f59-ade9-fe9580328ebc" />

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
<img width="343" height="304" alt="Screenshot 2026-05-29 204431" src="https://github.com/user-attachments/assets/1153ee30-adce-4292-87ce-2ad58c6dfc76" />

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
<img width="374" height="318" alt="Screenshot 2026-05-29 204524" src="https://github.com/user-attachments/assets/319d0c00-5d17-4245-828b-64a447f44e71" />

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
<img width="339" height="171" alt="Screenshot 2026-05-29 204549" src="https://github.com/user-attachments/assets/dcc8bbd3-1d05-4421-9411-eb6b80d984e8" />

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
 <img width="395" height="220" alt="Screenshot 2026-05-29 204946" src="https://github.com/user-attachments/assets/254e6f91-1837-47cd-a288-85e2c322f8ff" />

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
<img width="284" height="175" alt="Screenshot 2026-05-29 205000" src="https://github.com/user-attachments/assets/2a029e6c-1af1-4b90-9624-52f6ef913e64" />
 
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
<img width="429" height="130" alt="Screenshot 2026-05-29 205503" src="https://github.com/user-attachments/assets/66e54e5e-c2e5-4b4c-a02a-8a0de016efed" />

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
<img width="275" height="158" alt="Screenshot 2026-05-29 205540" src="https://github.com/user-attachments/assets/5bde3c5c-a696-4069-b275-92a9d6423682" />

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
<img width="230" height="134" alt="Screenshot 2026-05-29 205554" src="https://github.com/user-attachments/assets/b711a876-f052-4f0a-b07a-c2f4f9a569e3" />

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
<img width="273" height="134" alt="Screenshot 2026-05-29 205822" src="https://github.com/user-attachments/assets/4fdf9921-246e-400b-9d5e-cd8d8c26ff43" />

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
<img width="240" height="198" alt="Screenshot 2026-05-29 205845" src="https://github.com/user-attachments/assets/e44753ea-928c-4b95-ba3d-4cbdb970d570" />

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
<img width="323" height="216" alt="Screenshot 2026-05-29 205908" src="https://github.com/user-attachments/assets/61c9f5d4-ec6c-45fd-8930-e347417421e4" />

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
 <img width="323" height="216" alt="Screenshot 2026-05-29 205908" src="https://github.com/user-attachments/assets/9192485e-e1a8-4872-b3a5-e397cbdf4bbc" />

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
<img width="337" height="128" alt="Screenshot 2026-05-29 205928" src="https://github.com/user-attachments/assets/9599deb7-f533-435f-83f0-0afc69d48d17" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="344" height="114" alt="Screenshot 2026-05-29 205946" src="https://github.com/user-attachments/assets/d4aab416-098b-4229-80cf-187480dca533" />

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
<img width="392" height="241" alt="Screenshot 2026-05-29 210307" src="https://github.com/user-attachments/assets/1666deea-582e-4359-8713-f2250ad0c0e0" />

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
<img width="268" height="124" alt="Screenshot 2026-05-29 210345" src="https://github.com/user-attachments/assets/d1a66902-ec4a-452e-acea-ccef6335daee" />

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
<img width="266" height="132" alt="Screenshot 2026-05-29 210403" src="https://github.com/user-attachments/assets/1287845b-6513-4740-b6dd-911bf8695025" />

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
 <img width="266" height="132" alt="Screenshot 2026-05-29 210403" src="https://github.com/user-attachments/assets/47eacec8-4f80-429b-bb39-832af35e111c" />

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
 <img width="288" height="263" alt="Screenshot 2026-05-29 210420" src="https://github.com/user-attachments/assets/4250e9fa-4fe6-4a48-8c52-164078fc0199" />

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
<img width="322" height="321" alt="Screenshot 2026-05-29 210437" src="https://github.com/user-attachments/assets/84df9e85-aa0c-4c5f-ac58-a8cb1f5aeb05" />

# RESULT:
The Commands are executed successfully.

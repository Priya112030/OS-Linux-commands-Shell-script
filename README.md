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
<img width="434" height="139" alt="image" src="https://github.com/user-attachments/assets/6100bd57-db8b-4835-8720-cda5abf185ea" />



cat < file2
## OUTPUT
<img width="432" height="175" alt="image" src="https://github.com/user-attachments/assets/edbc6f05-3338-4897-b7d9-40e9b90e906f" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="477" height="65" alt="image" src="https://github.com/user-attachments/assets/0864d7fd-97bf-42ef-bcf7-960fcaaada63" />

comm file1 file2
 ## OUTPUT
<img width="488" height="255" alt="image" src="https://github.com/user-attachments/assets/a62dd68f-5dc8-41be-98cb-0b2895644a4c" />

 
diff file1 file2
## OUTPUT
<img width="455" height="337" alt="image" src="https://github.com/user-attachments/assets/c1b34d54-e3ea-40ee-bceb-2d7577b28c6b" />


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
<img width="459" height="88" alt="image" src="https://github.com/user-attachments/assets/906ebf86-e340-4c8e-8583-5b3fe99cf2b8" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="495" height="111" alt="image" src="https://github.com/user-attachments/assets/62c89d47-3c91-444a-ba2f-e0bf2ddb161a" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="547" height="117" alt="image" src="https://github.com/user-attachments/assets/62c0320a-9d0d-41e3-a5e9-67105515e806" />


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
<img width="453" height="70" alt="image" src="https://github.com/user-attachments/assets/f64bb5fb-c8a4-4a77-bd9f-7414ed783132" />



grep hello newfile 
## OUTPUT
<img width="458" height="64" alt="image" src="https://github.com/user-attachments/assets/fcd55b67-0afe-4ea9-8776-59821c192216" />




grep -v hello newfile 
## OUTPUT
<img width="458" height="64" alt="image" src="https://github.com/user-attachments/assets/1835cb60-98b3-45ac-a0f3-6acab74044c6" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="516" height="87" alt="image" src="https://github.com/user-attachments/assets/0fec8bc3-0c72-467b-bf88-4959a5109d67" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="546" height="62" alt="image" src="https://github.com/user-attachments/assets/7cf2500a-6dd6-48a5-8fa5-32086a032d13" />




grep -R ubuntu /etc
## OUTPUT
<img width="801" height="263" alt="image" src="https://github.com/user-attachments/assets/8e2c5d3e-33e5-4bb9-8b16-57c90e03e0d6" />



grep -w -n world newfile   
## OUTPUT
<img width="639" height="82" alt="image" src="https://github.com/user-attachments/assets/1e587c42-ce85-440d-8de4-60d5451e19eb" />


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
<img width="529" height="90" alt="image" src="https://github.com/user-attachments/assets/f738f1ca-0104-4b09-a915-cb3fd0a8a16f" />



egrep -w '(H|h)ello' newfile 
## OUTPUT



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="548" height="111" alt="image" src="https://github.com/user-attachments/assets/6bd8e76e-058e-4cff-bdf9-291c1cd82f36" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="481" height="56" alt="image" src="https://github.com/user-attachments/assets/c4e75907-f796-46e9-b69e-620eb4817bfb" />



egrep '(world$)' newfile 
## OUTPUT
<img width="516" height="79" alt="image" src="https://github.com/user-attachments/assets/8ac1ddf1-42a9-451d-97b1-2fc3efa3f3d2" />



egrep '(World$)' newfile 
## OUTPUT
<img width="566" height="71" alt="image" src="https://github.com/user-attachments/assets/2bcc6749-db12-4f1b-8718-94944caf6833" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="556" height="111" alt="image" src="https://github.com/user-attachments/assets/aa3db753-c82d-4633-b0a5-fd3f79b40c87" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="533" height="67" alt="image" src="https://github.com/user-attachments/assets/eb5ce3b1-cd84-4e3f-be0e-9c11e0423b56" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="523" height="57" alt="image" src="https://github.com/user-attachments/assets/bf1210e8-f59b-4414-9fce-27a55e35d81b" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="529" height="61" alt="image" src="https://github.com/user-attachments/assets/18f791fc-1f17-4490-a48a-0e0261fc9393" />


egrep l{2} newfile
## OUTPUT
<img width="534" height="76" alt="image" src="https://github.com/user-attachments/assets/b76224c8-061b-4e67-a9dc-d74721d3e392" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="483" height="104" alt="image" src="https://github.com/user-attachments/assets/e7b44cbc-7e84-49e6-8669-184cb86f93aa" />


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
<img width="492" height="59" alt="image" src="https://github.com/user-attachments/assets/9575ebc0-692e-44fd-afe4-4eaa7ccf8dac" />



sed -n -e '$p' file23
## OUTPUT
<img width="508" height="63" alt="image" src="https://github.com/user-attachments/assets/a0b4cc60-3fc3-4193-b478-c508a3f2af04" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="538" height="255" alt="image" src="https://github.com/user-attachments/assets/596ab8eb-7da5-4309-8c32-e9b664e0b08c" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="534" height="258" alt="image" src="https://github.com/user-attachments/assets/8fe8ed32-b481-42c8-980c-ce14afa38a7c" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="536" height="86" alt="image" src="https://github.com/user-attachments/assets/141e08d6-d476-4eaa-8c74-0058de9eef4c" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="521" height="177" alt="image" src="https://github.com/user-attachments/assets/2b3cd973-2b70-46d4-a412-5a77c50f96a1" />


sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="515" height="126" alt="image" src="https://github.com/user-attachments/assets/b7fabde6-4e9f-4b08-ae72-7c95b6aac6e6" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="547" height="247" alt="image" src="https://github.com/user-attachments/assets/3c953234-c42a-437e-9ba9-7be4adc6bb08" />



seq 10 
## OUTPUT
<img width="509" height="308" alt="image" src="https://github.com/user-attachments/assets/7ffa39ee-f88a-4c98-a095-5fde74cf6e3e" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="491" height="117" alt="image" src="https://github.com/user-attachments/assets/ad32a92a-d343-4595-8726-6c651a0413a5" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="492" height="108" alt="image" src="https://github.com/user-attachments/assets/debb9ae2-1688-467b-a8ee-699497d5d652" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="504" height="137" alt="image" src="https://github.com/user-attachments/assets/32dac2d3-1822-4caa-96f9-797ba123caa9" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="501" height="107" alt="image" src="https://github.com/user-attachments/assets/eb09aaba-c834-492d-bf64-3fc80db8cd17" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="490" height="114" alt="image" src="https://github.com/user-attachments/assets/d57bebec-c9a0-4512-80f7-f051785d3f2f" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="551" height="116" alt="image" src="https://github.com/user-attachments/assets/c4f75a58-9cbc-47f2-9249-03b1172fd1b6" />



sed -n '2,4{s/$/*/;p}' file23
<img width="514" height="116" alt="image" src="https://github.com/user-attachments/assets/27e4158a-116b-41c2-9c6a-7d629cd9aba4" />


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
<img width="527" height="175" alt="image" src="https://github.com/user-attachments/assets/9014064a-8bf8-4b88-9291-fc4ca41cc2c0" />


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
<img width="444" height="167" alt="image" src="https://github.com/user-attachments/assets/930f1817-10a2-40de-b697-6f86bef96018" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="605" height="243" alt="image" src="https://github.com/user-attachments/assets/118bfcfa-eddf-4ecd-bd3d-2d225b86e281" />

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
<img width="493" height="110" alt="image" src="https://github.com/user-attachments/assets/6b692b9f-bbc0-43ef-9eb5-40e2467ca453" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="634" height="113" alt="image" src="https://github.com/user-attachments/assets/1863ca98-19d9-44bd-9b25-78961931f1af" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="556" height="373" alt="image" src="https://github.com/user-attachments/assets/581763be-3246-49dc-a43d-5504f2e98214" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="694" height="494" alt="image" src="https://github.com/user-attachments/assets/ce91e9e9-4f24-4355-9068-03dd789c5e54" />


tar -xvf backup.tar
## OUTPUT
<img width="800" height="311" alt="image" src="https://github.com/user-attachments/assets/7a1d848f-57cf-4901-b0aa-244ff2d9e4cc" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="651" height="46" alt="image" src="https://github.com/user-attachments/assets/04b78f71-8b27-423d-9074-e074e552590b" />
 
gunzip backup.tar.gz
## OUTPUT
<img width="793" height="121" alt="image" src="https://github.com/user-attachments/assets/0df981f1-304b-4858-8dc5-c42b5d837415" />
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="796" height="117" alt="image" src="https://github.com/user-attachments/assets/3b472ddb-67bc-4d64-a013-68ccf2e3c874" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="699" height="174" alt="image" src="https://github.com/user-attachments/assets/a7a11400-4646-4302-ac03-2fc7a6085545" />


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
<img width="805" height="148" alt="image" src="https://github.com/user-attachments/assets/4d6759d5-cb45-4dc3-b58f-8f7db33c6695" />

 
ls file1
## OUTPUT
<img width="668" height="153" alt="image" src="https://github.com/user-attachments/assets/921865dd-ea26-41d2-b779-82331b231f59" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="805" height="157" alt="image" src="https://github.com/user-attachments/assets/0caa4ea2-2bee-453c-9b05-e8c11315cfc0" />
 
abcd
 
echo $?
 ## OUTPUT
<img width="716" height="156" alt="image" src="https://github.com/user-attachments/assets/86e398d4-f0e7-449c-b8d2-f6230f392883" />


 
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
<img width="703" height="197" alt="image" src="https://github.com/user-attachments/assets/fae5be74-3890-47bf-96c2-7edd4576ad92" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="657" height="90" alt="image" src="https://github.com/user-attachments/assets/e8611ca2-54d2-44cb-8c2e-26495d9dfd19" />


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
<img width="654" height="71" alt="image" src="https://github.com/user-attachments/assets/fbe0e3b2-51cf-4300-87cd-9353260fffc1" />

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
<img width="646" height="437" alt="image" src="https://github.com/user-attachments/assets/b59d7562-9e0f-4078-8c0d-720897ea8784" />



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
<img width="676" height="100" alt="image" src="https://github.com/user-attachments/assets/94f67e72-0809-4dda-bb41-4f01fe0a0d22" />

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
<img width="664" height="143" alt="image" src="https://github.com/user-attachments/assets/664b0a86-debf-4fb9-8224-f97ee8653d2f" />


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
<img width="660" height="73" alt="image" src="https://github.com/user-attachments/assets/840ecfb4-b9a3-4611-860f-9e872602469f" />
 
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
 <img width="662" height="239" alt="image" src="https://github.com/user-attachments/assets/dc9a5db7-70a3-46f9-8d40-f1935ab8437b" />

 
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
 <img width="703" height="126" alt="image" src="https://github.com/user-attachments/assets/a319477f-8912-4743-ac87-7c98bd6c1c2f" />

 
 
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
 <img width="633" height="220" alt="image" src="https://github.com/user-attachments/assets/aba340ef-0df0-40ce-be37-f9caeb8084f0" />

 
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
 <img width="731" height="176" alt="image" src="https://github.com/user-attachments/assets/5440df39-cd8b-465a-974e-22a0ebc57bdb" />

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
<img width="512" height="179" alt="image" src="https://github.com/user-attachments/assets/c72bddc1-fe75-4d14-b822-49f8fa5f7392" />

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
<img width="784" height="260" alt="image" src="https://github.com/user-attachments/assets/e71d3b25-e9b1-4888-8b0f-2e0c1d2665fa" />


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
<img width="620" height="220" alt="image" src="https://github.com/user-attachments/assets/4ca5fee1-02bc-442e-9c72-acadc7848acb" />

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
<img width="591" height="214" alt="image" src="https://github.com/user-attachments/assets/914d80bf-cb20-4630-8ccc-0ec413545c43" />

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
<img width="625" height="413" alt="image" src="https://github.com/user-attachments/assets/719573ec-a023-4594-9066-cd1063a16517" />

 
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
 <img width="602" height="179" alt="image" src="https://github.com/user-attachments/assets/5278af62-e7fb-444b-b51d-d5b26810678d" />

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
 <img width="665" height="214" alt="image" src="https://github.com/user-attachments/assets/cb6d1f68-7d6b-44b4-bf93-3df33b632e53" />

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
<img width="569" height="115" alt="image" src="https://github.com/user-attachments/assets/f92fbe32-5d3d-471e-850b-85d5ae0c8ad9" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="562" height="113" alt="image" src="https://github.com/user-attachments/assets/d317cc40-f643-4089-9374-8eb2e9d0b9a7" />



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
<img width="602" height="63" alt="image" src="https://github.com/user-attachments/assets/d8521342-1e30-45b4-b6e9-ac8add35b8aa" />

 
 ./funcex.sh 1 2
<img width="799" height="38" alt="image" src="https://github.com/user-attachments/assets/f1503332-b30f-4f9b-961d-eda98b7bb4ad" />

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
 <img width="627" height="175" alt="image" src="https://github.com/user-attachments/assets/390c5f75-aa9d-490a-afd3-03da3df67be2" />

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
<img width="549" height="139" alt="image" src="https://github.com/user-attachments/assets/155ea8bf-aa4a-4a63-a874-d77959d787f1" />


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
 <img width="579" height="441" alt="image" src="https://github.com/user-attachments/assets/768cc46a-6d43-4535-9939-19d5c1d29eee" />

 
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
 <img width="554" height="351" alt="image" src="https://github.com/user-attachments/assets/8b14b79d-0593-4116-8d0f-887898d90385" />

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
<img width="557" height="142" alt="image" src="https://github.com/user-attachments/assets/66cb6b3d-b834-4165-85aa-49deaeb1a206" />


# RESULT:
The Commands are executed successfully.

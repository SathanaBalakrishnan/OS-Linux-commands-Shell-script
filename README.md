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

<img width="731" height="237" alt="image" src="https://github.com/user-attachments/assets/5bdb553e-6972-478e-bad9-e5484ba716b5" />


cat < file2
## OUTPUT
<img width="685" height="277" alt="image" src="https://github.com/user-attachments/assets/b081e55c-0cce-428e-9ddb-07f767916f6c" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="615" height="47" alt="image" src="https://github.com/user-attachments/assets/21b16204-7ef1-4c9b-b080-626c48d79755" />
 
comm file1 file2
 ## OUTPUT
<img width="671" height="237" alt="image" src="https://github.com/user-attachments/assets/3b35be42-6d90-4416-bc27-8f595bca1e11" />

 
diff file1 file2
## OUTPUT
<img width="642" height="235" alt="image" src="https://github.com/user-attachments/assets/1eec5eff-afaa-40c1-8912-5004d2452fe9" />


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

cut -d "|" -f 1 file22

cut -d "|" -f 2 file22
## OUTPUT
<img width="623" height="72" alt="image" src="https://github.com/user-attachments/assets/73893bee-e3ee-4394-80d3-e010f4d1c0c2" />


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
grep hello newfile 
## OUTPUT

<img width="632" height="190" alt="image" src="https://github.com/user-attachments/assets/153b0853-ae4f-42ad-b987-148e337fd978" />



grep -v hello newfile 
## OUTPUT
<img width="625" height="62" alt="image" src="https://github.com/user-attachments/assets/0f264106-2800-4131-9f85-b4055c75ecfc" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="742" height="76" alt="image" src="https://github.com/user-attachments/assets/d4db8097-0fe2-4545-976b-49c17b6f3c12" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="831" height="47" alt="image" src="https://github.com/user-attachments/assets/d6f47280-75c0-4746-bc01-6a4bb86df0de" />



grep -R ubuntu /etc
## OUTPUT
<img width="945" height="912" alt="image" src="https://github.com/user-attachments/assets/67e4d614-678e-4602-abd3-a7aa1c09ecb7" />



grep -w -n world newfile   
## OUTPUT

<img width="750" height="76" alt="image" src="https://github.com/user-attachments/assets/cfddc25c-6ed3-4a7b-9ed4-6ed7372fc8cb" />

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

<img width="730" height="75" alt="image" src="https://github.com/user-attachments/assets/e5377e7d-f8d6-4c8b-8bb6-c8cde59f529c" />


egrep -w '(H|h)ello' newfile 
egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="898" height="73" alt="image" src="https://github.com/user-attachments/assets/8f182e13-a45d-4bbc-9ecc-6c99f56d0e54" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="700" height="37" alt="image" src="https://github.com/user-attachments/assets/6aa529de-f302-475d-8d41-dea4a65b9428" />


egrep '(world$)' newfile 
egrep '(World$)' newfile
## OUTPUT

<img width="620" height="87" alt="image" src="https://github.com/user-attachments/assets/90328e9e-17e7-4354-90ef-f2872f412499" />




egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="801" height="100" alt="image" src="https://github.com/user-attachments/assets/6b90208d-b7d5-454c-8640-68b44042407a" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="717" height="57" alt="image" src="https://github.com/user-attachments/assets/70b1e9b3-6a6e-4224-900f-dead1480ee38" />



egrep 'Linux.*world' newfile 
## OUTPUT

<img width="703" height="50" alt="image" src="https://github.com/user-attachments/assets/67ccc17b-f0af-4469-b796-3735569de0db" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="680" height="42" alt="image" src="https://github.com/user-attachments/assets/7e1a4d73-6cd2-4724-b5c0-4c102ea173dc" />


egrep l{2} newfile
## OUTPUT
<img width="622" height="67" alt="image" src="https://github.com/user-attachments/assets/a8830003-7903-409a-b424-96cc2e316b1b" />



egrep 's{1,2}' newfile
## OUTPUT 

<img width="642" height="103" alt="image" src="https://github.com/user-attachments/assets/64f2392b-9bb9-49fb-9bd7-ab19be753961" />

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
<img width="670" height="47" alt="image" src="https://github.com/user-attachments/assets/aced9e93-f30b-4455-a774-08b6a0a12963" />



sed -n -e '$p' file23
## OUTPUT

<img width="791" height="43" alt="image" src="https://github.com/user-attachments/assets/9b711a5e-e09b-4b9f-ba9a-39e1eca7f21e" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="876" height="210" alt="image" src="https://github.com/user-attachments/assets/5fca8bb4-dfe4-4cbd-a13b-f19912387aee" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="768" height="215" alt="image" src="https://github.com/user-attachments/assets/d4fc4b23-51f1-43a0-ada5-dc36c8b40add" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="742" height="220" alt="image" src="https://github.com/user-attachments/assets/4893589a-cd41-4217-bab2-ee0c2acc9059" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="628" height="140" alt="image" src="https://github.com/user-attachments/assets/aeb25b12-2fa8-4b08-845b-5c0320aaa127" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="763" height="91" alt="image" src="https://github.com/user-attachments/assets/c918e730-949d-47be-adc9-7125af6b89f4" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


<img width="883" height="75" alt="image" src="https://github.com/user-attachments/assets/56a3779e-ac94-4041-9cfe-1618659342fa" />

seq 10 
## OUTPUT

<img width="625" height="257" alt="image" src="https://github.com/user-attachments/assets/25b59d86-0b9f-4691-b201-636dbcbf2532" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="756" height="92" alt="image" src="https://github.com/user-attachments/assets/f2e36fab-f053-408c-8203-f998447b3d02" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="662" height="97" alt="image" src="https://github.com/user-attachments/assets/6a6997e5-b4c9-448a-996d-fba3b533ad1e" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="763" height="127" alt="image" src="https://github.com/user-attachments/assets/f8c15b4e-d743-4980-ac5e-9ef004e9d954" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="707" height="90" alt="image" src="https://github.com/user-attachments/assets/c958bf19-d442-4caa-880e-c7390aadd715" />

seq 10 | sed '2,9c hello'
## OUTPUT

<img width="793" height="98" alt="image" src="https://github.com/user-attachments/assets/08d415a3-4890-48e7-9e7c-dbe7ee46a2fa" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


<img width="741" height="102" alt="image" src="https://github.com/user-attachments/assets/5ab2a3f7-89d0-4a3d-ad45-b583743b42ad" />

sed -n '2,4{s/$/*/;p}' file23

<img width="747" height="101" alt="image" src="https://github.com/user-attachments/assets/c6b6e27b-a3db-4db5-bccc-aa781dcf1815" />

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

<img width="582" height="140" alt="image" src="https://github.com/user-attachments/assets/857693e5-10ae-49d8-bf92-784c6785acb2" />

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



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="862" height="215" alt="image" src="https://github.com/user-attachments/assets/08415460-7d82-44b7-a50c-255df8fa2256" />

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
<img width="696" height="90" alt="image" src="https://github.com/user-attachments/assets/5addb61f-9af3-4a9f-a8dd-be439a539b14" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="798" height="102" alt="image" src="https://github.com/user-attachments/assets/d950f8bf-aa60-403b-8288-9898cf3af028" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="912" height="575" alt="image" src="https://github.com/user-attachments/assets/3ed950ee-e42b-4441-a045-2b12678e60e7" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="820" height="680" alt="image" src="https://github.com/user-attachments/assets/3b927c05-f87f-4a61-a742-4e68fa0b40a5" />


tar -xvf backup.tar
## OUTPUT
<img width="762" height="700" alt="image" src="https://github.com/user-attachments/assets/86ab8102-b5fc-489c-8adb-8a6b739c4e26" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="666" height="67" alt="image" src="https://github.com/user-attachments/assets/9c0c49ce-6690-420a-ba63-4b649ebd7690" />

gunzip backup.tar.gz
## OUTPUT
<img width="765" height="77" alt="image" src="https://github.com/user-attachments/assets/e8fe4dec-2c41-40cc-b211-83883d49d21c" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="807" height="143" alt="image" src="https://github.com/user-attachments/assets/b099d5d4-1040-40a0-aaa7-68a78eb396da" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="662" height="100" alt="image" src="https://github.com/user-attachments/assets/59ada6ec-22b4-4dae-822f-0e59debf8988" />

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
<img width="661" height="347" alt="image" src="https://github.com/user-attachments/assets/baaf2512-49e3-4b04-9c09-58db112d2b9d" />

 
ls file1
## OUTPUT
<img width="462" height="52" alt="image" src="https://github.com/user-attachments/assets/f7937a5f-3b2f-457b-a997-5b6f40bc9b7f" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="535" height="53" alt="image" src="https://github.com/user-attachments/assets/4552413d-0160-4439-869f-d9ebd9234fcd" />

abcd
 
echo $?
 ## OUTPUT

<img width="612" height="241" alt="image" src="https://github.com/user-attachments/assets/b52d7f7c-72b6-49c3-89f2-9c3640918abd" />

 
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




chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="576" height="77" alt="image" src="https://github.com/user-attachments/assets/456ccae6-909c-4f90-8351-20be41c5dc00" />


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
<img width="721" height="72" alt="image" src="https://github.com/user-attachments/assets/fc07d0e5-4293-4bec-bfc7-06b92e55c70f" />

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


<img width="657" height="402" alt="image" src="https://github.com/user-attachments/assets/ea247411-3271-4e9a-8a21-945183f7b22a" />

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
<img width="702" height="458" alt="image" src="https://github.com/user-attachments/assets/5a156b6b-ab18-495f-802d-682e70e7c2df" />

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
<img width="776" height="521" alt="image" src="https://github.com/user-attachments/assets/1b91e21b-a6c6-4445-a2b5-d637b84f4993" />

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

<img width="736" height="512" alt="image" src="https://github.com/user-attachments/assets/465aa0a8-3b10-48c6-a4ea-f94d7645785b" />

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
<img width="728" height="247" alt="image" src="https://github.com/user-attachments/assets/05c66596-460f-4768-84b4-2d1a3f6c9241" />

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
 ## Output
<img width="707" height="382" alt="image" src="https://github.com/user-attachments/assets/a5770c17-6805-4de7-8635-1fcad1399095" />

 
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
 ## Output
 <img width="682" height="491" alt="image" src="https://github.com/user-attachments/assets/c93c73dc-3605-4878-a7a2-683a637433c3" />

 
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
 ## Output
 <img width="761" height="347" alt="image" src="https://github.com/user-attachments/assets/19e246de-5f3c-496c-9004-9d9b7adf7bda" />

 
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
 ## Output
 <img width="831" height="347" alt="image" src="https://github.com/user-attachments/assets/50d81036-239f-4e6f-812f-e05e7ee168a7" />

 
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
 ## Output
 <img width="735" height="292" alt="image" src="https://github.com/user-attachments/assets/61a9dbe4-77f0-4d7a-a7eb-2ae89c5bad05" />

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
 ## Output
 <img width="657" height="302" alt="image" src="https://github.com/user-attachments/assets/3cc63fec-3610-4860-a586-5ff84b57d193" />

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
 ## Output
 <img width="836" height="343" alt="image" src="https://github.com/user-attachments/assets/a29b0a98-2067-463d-9d1d-8d7f74846cb7" />

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

<img width="721" height="393" alt="image" src="https://github.com/user-attachments/assets/762ff12c-674f-4268-9b7d-9d305e1a9079" />

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
<img width="617" height="315" alt="image" src="https://github.com/user-attachments/assets/ce2d4b5a-e225-4a68-a09b-ca4a254a0ba6" />

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
<img width="641" height="321" alt="image" src="https://github.com/user-attachments/assets/ee2e8670-e0ba-4473-85a4-c22c8d1691ba" />

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

 <img width="692" height="562" alt="image" src="https://github.com/user-attachments/assets/6cd280f6-ed02-460a-b68f-f572ec55cec1" />

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
 <img width="637" height="392" alt="image" src="https://github.com/user-attachments/assets/81e44916-9a67-40aa-a786-1dfb4a6f8974" />

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
 <img width="678" height="442" alt="image" src="https://github.com/user-attachments/assets/67f7eef3-0488-43cc-86e2-bccc1afd378a" />

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
<img width="625" height="235" alt="image" src="https://github.com/user-attachments/assets/faa5940a-1654-4b10-82ba-d98db6c8b69d" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="647" height="236" alt="image" src="https://github.com/user-attachments/assets/2cb97adc-4e5d-4266-85b7-3d993a029c70" />



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
<img width="717" height="430" alt="image" src="https://github.com/user-attachments/assets/24572e2e-0e88-4801-b3f1-2713a42baed2" />

 
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
 <img width="657" height="280" alt="image" src="https://github.com/user-attachments/assets/573f3882-f1cb-44a2-af58-fc0a44f62570" />

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
 <img width="702" height="412" alt="image" src="https://github.com/user-attachments/assets/c9bcb2f8-f889-4451-bd70-056d1e3da7ca" />

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
 
 <img width="817" height="550" alt="image" src="https://github.com/user-attachments/assets/7b03be4e-641b-446e-9d92-b2d500ec2e4d" />

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
 <img width="761" height="877" alt="image" src="https://github.com/user-attachments/assets/eeaa4642-bee2-4096-a735-5b25a7464001" />

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
<img width="815" height="767" alt="image" src="https://github.com/user-attachments/assets/39200d59-42ea-4040-95b4-88842eac994f" />


# RESULT:
The Commands are executed successfully.

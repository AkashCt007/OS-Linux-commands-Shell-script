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
<img width="419" height="196" alt="image" src="https://github.com/user-attachments/assets/a3787ce1-bec0-4721-af02-6e3268684192" />





cat < file2
## OUTPUT
<img width="399" height="198" alt="image" src="https://github.com/user-attachments/assets/0cf219bd-44a1-4e9b-89b2-922e5d2f2516" />



# Comparing Files
cmp file1 file2
## OUTPUT
<img width="378" height="80" alt="Screenshot 2025-09-02 112530" src="https://github.com/user-attachments/assets/49718ade-fc09-48f2-981f-9c3bbac0481f" />

 
comm file1 file2
 ## OUTPUT
<img width="417" height="225" alt="Screenshot 2025-09-02 112543" src="https://github.com/user-attachments/assets/7b6fefb7-3773-42b7-80e6-e4bcb0a84847" />

 
diff file1 file2
## OUTPUT
<img width="456" height="186" alt="Screenshot 2025-09-02 112557" src="https://github.com/user-attachments/assets/68b42d19-0365-4353-b7f6-1dff1b000673" />

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

<img width="384" height="104" alt="Screenshot 2025-09-02 112657" src="https://github.com/user-attachments/assets/d9c5c817-bde3-46b4-b05c-d3bb465fbbd9" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="384" height="104" alt="Screenshot 2025-09-02 112657" src="https://github.com/user-attachments/assets/9cab1955-4923-4a5a-8f75-9900c5473410" />



cut -d "|" -f 2 file22
## OUTPUT

<img width="384" height="104" alt="Screenshot 2025-09-02 112657" src="https://github.com/user-attachments/assets/4de6abe6-9f60-4df9-ac97-2c586b87bef6" />

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
<img width="323" height="82" alt="Screenshot 2025-09-02 113045" src="https://github.com/user-attachments/assets/2eb8f1ca-3b4a-44e7-a856-b1fd90000d78" />



grep hello newfile 
## OUTPUT
<img width="323" height="82" alt="Screenshot 2025-09-02 113045" src="https://github.com/user-attachments/assets/7004c56c-994a-49ce-beff-40b44966b7b6" />




grep -v hello newfile 
## OUTPUT

<img width="329" height="84" alt="Screenshot 2025-09-02 113059" src="https://github.com/user-attachments/assets/810c39b0-b1ba-4e79-831c-b4201dcb5e58" />


cat newfile | grep -i "hello"
## OUTPUT


<img width="384" height="125" alt="Screenshot 2025-09-02 113114" src="https://github.com/user-attachments/assets/84310ac0-c6a3-4713-b476-1f9e1af6c9c0" />


cat newfile | grep -i -c "hello"
## OUTPUT


<img width="384" height="125" alt="Screenshot 2025-09-02 113114" src="https://github.com/user-attachments/assets/a6020c90-ea37-46ae-bf44-0afc610f5f9c" />


grep -R ubuntu /etc
## OUTPUT
<img width="766" height="542" alt="Screenshot 2025-09-02 113127" src="https://github.com/user-attachments/assets/2632a362-4921-4af9-940b-710f983ff83a" />



grep -w -n world newfile   
## OUTPUT

<img width="299" height="104" alt="Screenshot 2025-09-02 113406" src="https://github.com/user-attachments/assets/f7a153d6-c189-4fca-b3fb-681e3dfedb59" />

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


<img width="398" height="111" alt="Screenshot 2025-09-02 113458" src="https://github.com/user-attachments/assets/809748eb-ab6b-4ed4-a121-81ab440d4478" />

egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="379" height="118" alt="Screenshot 2025-09-22 230416" src="https://github.com/user-attachments/assets/1f708f32-1395-417b-8b3c-a530db8dd055" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="493" height="98" alt="Screenshot 2025-09-22 230452" src="https://github.com/user-attachments/assets/6c047e90-6d41-4229-8331-62eb6d3e689e" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="369" height="82" alt="Screenshot 2025-09-22 230516" src="https://github.com/user-attachments/assets/2e4facd7-d9aa-4b9e-ae04-10ad40fb32af" />



egrep '(world$)' newfile 
## OUTPUT
<img width="313" height="102" alt="Screenshot 2025-09-10 103349" src="https://github.com/user-attachments/assets/045b0020-075f-4889-acb5-d355f6160d04" />



egrep '(World$)' newfile 
## OUTPUT
<img width="446" height="131" alt="image" src="https://github.com/user-attachments/assets/52f527da-4146-4b34-8562-9b258d931a65" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="381" height="129" alt="Screenshot 2025-09-10 103430" src="https://github.com/user-attachments/assets/678e4f17-1f53-4f62-9046-bcb10a6c6b0a" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="295" height="81" alt="Screenshot 2025-09-10 103441" src="https://github.com/user-attachments/assets/380f88b7-f9cf-4ed0-9ee0-9e573da5ffb9" />



egrep 'Linux.*world' newfile 
## OUTPUT

<img width="362" height="85" alt="Screenshot 2025-09-10 103457" src="https://github.com/user-attachments/assets/2d76d786-541d-45a8-bd00-dc056202cb3f" />

egrep 'Linux.*World' newfile 
## OUTPUT


<img width="422" height="78" alt="Screenshot 2025-09-10 103505" src="https://github.com/user-attachments/assets/fdf4b756-c0b5-4a06-a455-38b3b0a433e0" />

egrep l{2} newfile
## OUTPUT

<img width="340" height="108" alt="Screenshot 2025-09-10 103527" src="https://github.com/user-attachments/assets/e280a74c-0330-4f4d-8e37-7c4344de8edc" />



egrep 's{1,2}' newfile
## OUTPUT 


<img width="401" height="121" alt="Screenshot 2025-09-10 103547" src="https://github.com/user-attachments/assets/3dbc1b92-7464-4067-876d-e227abdefb91" />

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
	

<img width="323" height="80" alt="Screenshot 2025-09-10 103614" src="https://github.com/user-attachments/assets/36bc8258-3984-41b3-84b8-390776a28466" />


sed -n -e '$p' file23
## OUTPUT


<img width="312" height="83" alt="Screenshot 2025-09-10 103622" src="https://github.com/user-attachments/assets/8e85ae80-5257-4d4a-89f9-b4b134a53fab" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT


<img width="448" height="249" alt="Screenshot 2025-09-10 103633" src="https://github.com/user-attachments/assets/6ca08e93-2432-480d-be95-df98c9a9ab7b" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT


<img width="487" height="253" alt="Screenshot 2025-09-10 103649" src="https://github.com/user-attachments/assets/0babc823-0855-41d8-990f-0b734ed42ea6" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="502" height="254" alt="image" src="https://github.com/user-attachments/assets/db6a449a-120e-4297-9d3c-de686e743569" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="418" height="188" alt="Screenshot 2025-09-22 224427" src="https://github.com/user-attachments/assets/330810ec-33a8-446f-9860-81d799f6eb2d" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="384" height="140" alt="Screenshot 2025-09-22 224452" src="https://github.com/user-attachments/assets/fe9438b8-db15-4643-bd85-d357c6c51e1c" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


<img width="444" height="105" alt="Screenshot 2025-09-22 224526" src="https://github.com/user-attachments/assets/ef98e8af-637f-465c-9cc1-5f107205db84" />


seq 10 
## OUTPUT



<img width="362" height="307" alt="Screenshot 2025-09-22 224542" src="https://github.com/user-attachments/assets/d43cdc14-ecfd-443f-b667-dff0e742d788" />

seq 10 | sed -n '4,6p'
## OUTPUT


<img width="345" height="137" alt="Screenshot 2025-09-22 224610" src="https://github.com/user-attachments/assets/dc63935b-9594-495d-80ef-34ec37a072cb" />


seq 10 | sed -n '2,~4p'
## OUTPUT



<img width="441" height="130" alt="Screenshot 2025-09-22 224636" src="https://github.com/user-attachments/assets/3b4b34af-b500-4e59-8150-6d48729772e4" />

seq 3 | sed '2a hello'
## OUTPUT

<img width="347" height="158" alt="Screenshot 2025-09-22 224709" src="https://github.com/user-attachments/assets/920d4b60-5874-4923-a217-79332b1c0cd5" />



seq 2 | sed '2i hello'
## OUTPUT

<img width="370" height="136" alt="Screenshot 2025-09-22 224736" src="https://github.com/user-attachments/assets/b7114183-c85d-4a51-bc4d-a9e06c8245a1" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="372" height="130" alt="Screenshot 2025-09-22 224756" src="https://github.com/user-attachments/assets/4dd2042d-f4ae-4ef9-933d-9e92096b7bd5" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="522" height="133" alt="Screenshot 2025-09-22 224836" src="https://github.com/user-attachments/assets/7de3d82d-37e5-4e6b-b6f1-dbcbf7afa430" />



sed -n '2,4{s/$/*/;p}' file23

<img width="429" height="137" alt="Screenshot 2025-09-22 224915" src="https://github.com/user-attachments/assets/55794737-8cc9-494c-b7ec-d6444fe05925" />


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

<img width="357" height="180" alt="Screenshot 2025-09-10 112119" src="https://github.com/user-attachments/assets/a83c3f29-28c0-47ae-afc0-0a3a789e85ec" />


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


<img width="451" height="177" alt="Screenshot 2025-09-22 225130" src="https://github.com/user-attachments/assets/ac1c3faa-267f-4033-b068-809b5b397954" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

 <img width="486" height="252" alt="Screenshot 2025-09-10 112148" src="https://github.com/user-attachments/assets/9b0f32db-f625-43b1-8c20-f5265cc53a44" />


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

<img width="370" height="133" alt="Screenshot 2025-09-10 112445" src="https://github.com/user-attachments/assets/21e32b4a-19e5-4992-b987-ac3b0cd11382" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT


<img width="477" height="136" alt="Screenshot 2025-09-10 112943" src="https://github.com/user-attachments/assets/5e72f396-7869-4e3b-8f49-f2db881eaf82" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT


<img width="468" height="525" alt="Screenshot 2025-09-10 113144" src="https://github.com/user-attachments/assets/363f3976-6cbc-4d15-98ce-a099a5a6596e" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT



<img width="782" height="593" alt="Screenshot 2025-09-10 114353" src="https://github.com/user-attachments/assets/c5b67fb5-12b3-4ad0-b204-ab05f56f7f5b" />



tar -xvf backup.tar
## OUTPUT

<img width="427" height="529" alt="Screenshot 2025-09-10 113219" src="https://github.com/user-attachments/assets/b06d9253-95ff-4ed7-b3ea-f01ce2ba1840" />

gzip backup.tar

ls .gz
## OUTPUT


 <img width="407" height="126" alt="Screenshot 2025-09-10 114511" src="https://github.com/user-attachments/assets/9050b8a8-5827-412a-9db7-625f4fa5b9e0" />

gunzip backup.tar.gz
## OUTPUT


 <img width="407" height="126" alt="Screenshot 2025-09-10 114511" src="https://github.com/user-attachments/assets/11180149-0c66-4920-b4b5-c0074761f4d8" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 <img width="373" height="290" alt="image" src="https://github.com/user-attachments/assets/7bffa044-9ca4-48b8-bd0f-936fe78087b5" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="464" height="158" alt="Screenshot 2025-09-10 213209" src="https://github.com/user-attachments/assets/2a44d386-f9d0-43e4-a1c7-ea3cb044aad4" />


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

 <img width="635" height="630" alt="Screenshot 2025-09-10 213401" src="https://github.com/user-attachments/assets/153caaee-21e4-40c6-a335-333c651cbd7f" />

ls file1
## OUTPUT

<img width="412" height="381" alt="Screenshot 2025-09-16 102026" src="https://github.com/user-attachments/assets/34dac5bb-8c6b-4004-b463-2bbc995c661c" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

 <img width="412" height="381" alt="Screenshot 2025-09-16 102026" src="https://github.com/user-attachments/assets/c1d270c0-eaca-48a4-ac05-c2b4cabc2faf" />

abcd
 
echo $?
 ## OUTPUT

<img width="412" height="381" alt="Screenshot 2025-09-16 102026" src="https://github.com/user-attachments/assets/d8f0feae-c83a-4eaf-ae5b-1ff8cbdcf4a8" />


 
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

<img width="637" height="437" alt="Screenshot 2025-09-16 102543" src="https://github.com/user-attachments/assets/b03514dc-f992-4950-8383-44bbe61ebe4d" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


<img width="637" height="437" alt="Screenshot 2025-09-16 102543" src="https://github.com/user-attachments/assets/a6710b2e-f2bf-4f04-9d96-3d29cf67f9cd" />

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

<img width="624" height="307" alt="Screenshot 2025-09-16 102957" src="https://github.com/user-attachments/assets/3ac4f6d8-431a-4e68-b2e0-d35b5c68eafc" />

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

<img width="587" height="198" alt="Screenshot 2025-09-16 113509" src="https://github.com/user-attachments/assets/fa94ee2b-e3cf-4656-b213-fe9d4b432b17" />



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


<img width="382" height="154" alt="Screenshot 2025-09-16 113814" src="https://github.com/user-attachments/assets/41477c68-1b50-41b5-99a5-28054af9a07a" />


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

<img width="500" height="136" alt="Screenshot 2025-09-16 114938" src="https://github.com/user-attachments/assets/6f8d62b8-0dc7-4958-bee6-a061cbdaa641" />


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


<img width="650" height="581" alt="Screenshot 2025-09-17 111503" src="https://github.com/user-attachments/assets/72749c39-2472-47e8-bff5-c0038b4fb69e" />

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

<img width="629" height="425" alt="Screenshot 2025-09-17 111735" src="https://github.com/user-attachments/assets/cc59b900-1b6a-44fe-bdd7-f2e3f307cb16" />

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

 <img width="577" height="466" alt="Screenshot 2025-09-17 112047" src="https://github.com/user-attachments/assets/60632fe0-d138-4122-ba32-aa54bd77c3dd" />

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

 <img width="435" height="607" alt="Screenshot 2025-09-17 113938" src="https://github.com/user-attachments/assets/59e953a5-57e4-4334-97fe-a6c6230b7ee2" />

 
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
 

 <img width="391" height="448" alt="Screenshot 2025-09-17 114212" src="https://github.com/user-attachments/assets/73788e23-edfa-454d-82da-21220b1580de" />

 
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

 <img width="696" height="488" alt="Screenshot 2025-09-17 114424" src="https://github.com/user-attachments/assets/b77c4f74-cc92-4801-bc6b-9c58cc2f382e" />

 
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


 <img width="652" height="378" alt="Screenshot 2025-09-17 114639" src="https://github.com/user-attachments/assets/6d5f02f2-0cdd-492d-bb26-e7cf484e665e" />

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

<img width="652" height="378" alt="Screenshot 2025-09-17 114639" src="https://github.com/user-attachments/assets/4af211cb-1f6f-4000-81f5-3739facf94c3" />

 
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

<img width="571" height="381" alt="Screenshot 2025-09-17 114837" src="https://github.com/user-attachments/assets/3dddbc0f-e46b-437c-88ff-711b0e00ac7b" />

 
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

<img width="696" height="488" alt="Screenshot 2025-09-17 114424" src="https://github.com/user-attachments/assets/574c0d86-1d1d-484d-a40a-58d3bf5e6605" />

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

<img width="319" height="235" alt="Screenshot 2025-09-22 125806" src="https://github.com/user-attachments/assets/5fbff7e5-36eb-460b-a070-64f70268f4d7" />



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

<img width="293" height="199" alt="Screenshot 2025-09-22 130032" src="https://github.com/user-attachments/assets/da0c5101-5f10-4383-87c5-71ea7aabed64" />


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

<img width="306" height="183" alt="Screenshot 2025-09-22 130255" src="https://github.com/user-attachments/assets/11d70937-0df6-4a36-806d-edd8cabaf694" />

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
 


 <img width="387" height="373" alt="Screenshot 2025-09-22 130527" src="https://github.com/user-attachments/assets/7f1d04da-8e4e-42be-8479-dcbdf1eda676" />

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

<img width="320" height="138" alt="Screenshot 2025-09-22 130856" src="https://github.com/user-attachments/assets/79fed70f-7309-45f5-a096-98a55c743ede" />

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

 <img width="349" height="189" alt="Screenshot 2025-09-22 131205" src="https://github.com/user-attachments/assets/991fa7d1-6172-44dd-a151-a3df22ff75bf" />

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

<img width="496" height="378" alt="Screenshot 2025-09-22 131343" src="https://github.com/user-attachments/assets/42433fcc-9161-4533-a137-7008bc5fcc70" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT


<img width="374" height="155" alt="Screenshot 2025-09-22 131611" src="https://github.com/user-attachments/assets/70591556-7a08-4828-8292-9ffc3a685a02" />


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

<img width="342" height="85" alt="Screenshot 2025-09-22 211746" src="https://github.com/user-attachments/assets/3ce69808-bcc5-4bd4-afad-16688c05fdda" />

 
 ./funcex.sh 1 2

<img width="673" height="187" alt="Screenshot 2025-09-22 213506" src="https://github.com/user-attachments/assets/d93bda59-7bfc-46e0-a548-de1e78fbc514" />

 
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

<img width="347" height="410" alt="Screenshot 2025-09-22 213704" src="https://github.com/user-attachments/assets/8cfd04d8-9fe2-4152-a1bb-d153934dcca9" />

 
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
$ ./argshift.sh 10 20 30

<img width="359" height="152" alt="Screenshot 2025-09-22 214117" src="https://github.com/user-attachments/assets/2b9bf2f8-6b86-4eae-a8f9-3169bd951458" />


 
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
 

 <img width="456" height="415" alt="Screenshot 2025-09-22 214519" src="https://github.com/user-attachments/assets/cf3d72a6-00f1-4360-a624-866645011e80" />

 
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

 <img width="439" height="356" alt="Screenshot 2025-09-22 214937" src="https://github.com/user-attachments/assets/3e48b6b1-3cba-486a-adbd-13f5e79f2cfa" />

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


<img width="328" height="312" alt="Screenshot 2025-09-22 215454" src="https://github.com/user-attachments/assets/6ef6f01d-7981-4adb-9ce5-d51ae174d0db" />

# RESULT:
The Commands are executed successfully.

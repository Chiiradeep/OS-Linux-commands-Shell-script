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
<img width="460" height="157" alt="image" src="https://github.com/user-attachments/assets/c1790be8-3b3b-49c6-9263-ca64afc64330" />

cat < file2
## OUTPUT
<img width="530" height="182" alt="image" src="https://github.com/user-attachments/assets/c609006a-2ab5-4ccc-991c-86f2eecb144d" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="514" height="82" alt="image" src="https://github.com/user-attachments/assets/273f7547-5623-49d3-8c11-ed8413ba0755" />

comm file1 file2
 ## OUTPUT
<img width="548" height="360" alt="image" src="https://github.com/user-attachments/assets/7511f0e2-2b1a-409f-bdf1-3077ed8eace9" />

 
diff file1 file2
## OUTPUT
<img width="473" height="273" alt="image" src="https://github.com/user-attachments/assets/d5e65e23-191e-45c0-991b-0e2f8e94b431" />

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
<img width="398" height="105" alt="image" src="https://github.com/user-attachments/assets/2eb3c282-fa71-4e2a-badc-05e532f50eef" />

cut -d "|" -f 1 file22
## OUTPUT
<img width="441" height="143" alt="image" src="https://github.com/user-attachments/assets/00ecd03f-7a4a-4e36-8354-75992e6b9a18" />

cut -d "|" -f 2 file22
## OUTPUT
<img width="481" height="156" alt="image" src="https://github.com/user-attachments/assets/fb5f3b69-3b04-403b-aa8b-5a6af44b8364" />

cat > newfile 
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
<img width="468" height="85" alt="image" src="https://github.com/user-attachments/assets/76254c55-f527-4d83-af81-0f3e95a3fa15" />

grep hello newfile 
## OUTPUT

<img width="382" height="82" alt="image" src="https://github.com/user-attachments/assets/cd281ad6-600e-4b0f-ae7f-387d09652a70" />

grep -v hello newfile 
## OUTPUT

<img width="395" height="75" alt="image" src="https://github.com/user-attachments/assets/aa2731ca-023c-43d5-81e0-49fc04528fef" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="429" height="105" alt="image" src="https://github.com/user-attachments/assets/c9d77d6a-382e-411e-865f-4be5f788a55e" />

cat newfile | grep -i -c "hello"
## OUTPUT

<img width="470" height="77" alt="image" src="https://github.com/user-attachments/assets/5ea1c295-4b29-4d50-889b-df9e4eb383d8" />

grep -R ubuntu /etc
## OUTPUT

<img width="809" height="600" alt="image" src="https://github.com/user-attachments/assets/e967f4da-253a-486b-9438-7f45ad669568" />


grep -w -n world newfile   
## OUTPUT
<img width="437" height="106" alt="image" src="https://github.com/user-attachments/assets/702fb23d-f695-4efa-b809-3342ac7a31b8" />

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

<img width="508" height="109" alt="image" src="https://github.com/user-attachments/assets/eac94bef-cb03-42c2-8b1b-27e55f9b2556" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="398" height="99" alt="image" src="https://github.com/user-attachments/assets/646f0fb8-5d43-4c4d-986f-d2b1216391ea" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="468" height="101" alt="image" src="https://github.com/user-attachments/assets/ce8e7c9d-a202-4f1b-b0ca-69cc36fc233b" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="421" height="81" alt="image" src="https://github.com/user-attachments/assets/b96968ca-df56-43cc-bd15-db763daa972a" />


egrep '(world$)' newfile 
## OUTPUT

<img width="415" height="107" alt="image" src="https://github.com/user-attachments/assets/fe001551-6421-4408-bb8a-7e68ff80a4b9" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="562" height="126" alt="image" src="https://github.com/user-attachments/assets/01c62c9b-ebeb-4476-91b5-1620e0525f7a" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="350" height="85" alt="image" src="https://github.com/user-attachments/assets/fc1ac886-e12e-4cab-90bd-b06c277b2d5b" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="459" height="89" alt="image" src="https://github.com/user-attachments/assets/a051068e-33ec-4c5d-922a-8fd1df98d18a" />


egrep l{2} newfile
## OUTPUT

<img width="487" height="106" alt="image" src="https://github.com/user-attachments/assets/3af3cd96-328a-4574-8dc6-a5e389e352cd" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="434" height="135" alt="image" src="https://github.com/user-attachments/assets/f12e020e-cd64-448f-82cf-cfe995c20d77" />


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

<img width="526" height="73" alt="image" src="https://github.com/user-attachments/assets/bdef8c31-8d78-4f91-a1ab-c65e65c9cec2" />


sed -n -e '$p' file23
## OUTPUT

<img width="346" height="91" alt="image" src="https://github.com/user-attachments/assets/8afe6df6-752c-4b82-b809-ac37834b893c" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="517" height="251" alt="image" src="https://github.com/user-attachments/assets/efeb9015-8ae2-4974-9024-76c0e347d7d5" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="502" height="256" alt="image" src="https://github.com/user-attachments/assets/9b13e02a-8c0a-4363-9a3e-f935cc790af6" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="540" height="253" alt="image" src="https://github.com/user-attachments/assets/d803fb84-3dce-42b1-9f59-50252bf43603" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="434" height="173" alt="image" src="https://github.com/user-attachments/assets/3ea22554-fcd3-4fae-b078-04ba671ac227" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="427" height="129" alt="image" src="https://github.com/user-attachments/assets/53beb68e-f42f-466d-96a8-4e6bd897eebd" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="572" height="101" alt="image" src="https://github.com/user-attachments/assets/820adedb-fb95-40b1-be6a-254d481d493e" />


seq 10 
## OUTPUT

<img width="497" height="305" alt="image" src="https://github.com/user-attachments/assets/02a400af-c95f-4aca-94f2-cc532d93ee11" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="500" height="138" alt="image" src="https://github.com/user-attachments/assets/87578ff1-a04d-47d1-84a8-506ec98585ab" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="396" height="125" alt="image" src="https://github.com/user-attachments/assets/5409dd66-9ec1-4f09-9a89-15cef67387ab" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="333" height="153" alt="image" src="https://github.com/user-attachments/assets/cb62f5a0-7431-4132-8050-af195df851dd" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="384" height="128" alt="image" src="https://github.com/user-attachments/assets/cad2ca5d-c3f0-4d87-b805-601c4088a10a" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="420" height="126" alt="image" src="https://github.com/user-attachments/assets/1b758780-6769-41a2-8e63-20f5d804bd58" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="417" height="126" alt="image" src="https://github.com/user-attachments/assets/1318869b-f013-439b-b92f-444692d44b98" />



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
<img width="619" height="184" alt="image" src="https://github.com/user-attachments/assets/8e9ca64b-2f0e-4dec-9fea-aaa6ea39e481" />


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

<img width="505" height="174" alt="image" src="https://github.com/user-attachments/assets/11ec67ae-e8d8-4488-8be5-392ca6d149a3" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="549" height="255" alt="image" src="https://github.com/user-attachments/assets/b6e3fcb7-6e3e-41db-b05b-fd1c9cb2f34e" />

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

<img width="411" height="150" alt="image" src="https://github.com/user-attachments/assets/7bc641e5-a3eb-4be1-8dcc-36960e32c62a" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="560" height="151" alt="image" src="https://github.com/user-attachments/assets/7af5b904-f3b7-462b-9ea3-ed2f22c355d2" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="671" height="592" alt="image" src="https://github.com/user-attachments/assets/be07abf9-4638-47ff-b1da-c5360ed30e45" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="748" height="603" alt="image" src="https://github.com/user-attachments/assets/28002af5-8715-4f2a-aac9-e4e6a49fed13" />


tar -xvf backup.tar
## OUTPUT
<img width="570" height="621" alt="image" src="https://github.com/user-attachments/assets/1bdd0e1a-e35d-4fc9-afa4-af610d08df85" />


gzip backup.tar

ls .gz
## OUTPUT
 <img width="558" height="180" alt="image" src="https://github.com/user-attachments/assets/30db76c6-2b33-476e-b033-5c93d9a0d837" />
 
 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="558" height="288" alt="image" src="https://github.com/user-attachments/assets/1aee7cfb-cfa2-4225-acc3-4317cdfb616c" />


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

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
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

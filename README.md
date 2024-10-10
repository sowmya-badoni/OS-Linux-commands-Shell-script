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
![output]![output1_1](https://github.com/user-attachments/assets/3a093d9a-5459-4b66-ad59-b9383d3e30bc)



cat < file2
## OUTPUT
![output]![output1_2](https://github.com/user-attachments/assets/05744bfd-6d12-462b-bdbe-da0dfb2fef9f)


# Comparing Files
cmp file1 file2
## OUTPUT
![output](./output1_3.png)
comm file1 file2
 ## OUTPUT
![output](./output1_4.png)
 
diff file1 file2
## OUTPUT
![output](./output1_5.png)

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
![output](./output1_6.png)



cut -d "|" -f 1 file22
## OUTPUT
![output](./output1_7.png)


cut -d "|" -f 2 file22
## OUTPUT
![output](./output1_8.png)

cat < newfile 
```
Hello world
hello world
^d
```
cat > newfile 
```
Hello world
hello world
```
grep Hello newfile 
## OUTPUT
![output]![output1_9](https://github.com/user-attachments/assets/b551ce64-1286-4c5f-9386-ee5b1f8b1f1c)



grep hello newfile 
## OUTPUT
![output]!![output1_10](https://github.com/user-attachments/assets/25715c73-1faf-43ac-b691-25e4cc580e50)





grep -v hello newfile 
## OUTPUT
![output]![output1_11](https://github.com/user-attachments/assets/5e4731a1-5657-41d8-8ac1-0cd82348bace)



cat newfile | grep -i "hello"
## OUTPUT
![output]![output1_12](https://github.com/user-attachments/assets/0820b89c-598c-43a3-8a29-7ffec77217bb)




cat newfile | grep -i -c "hello"
## OUTPUT
![output]![output1_13](https://github.com/user-attachments/assets/60c614d1-2b1d-4835-a63e-2f37f70fda92)




grep -R ubuntu /etc
## OUTPUT
![output]![output1_14](https://github.com/user-attachments/assets/c15f8e6d-7092-4137-bc6d-1d40f4dd7e81)



grep -w -n world newfile   
## OUTPUT
![output]![output1_15](https://github.com/user-attachments/assets/bdb7f3be-e5ba-41dc-a5b8-16bff93067ae)


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
![output]![output1_16](https://github.com/user-attachments/assets/c9ed5649-67d3-42bb-8837-5b2c9cc6c4b4)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![output]![output1_17](https://github.com/user-attachments/assets/052e09da-4b8a-4449-89f3-7dece27e078d)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![output]![output1_18](https://github.com/user-attachments/assets/3ca547f5-5356-48ac-835b-da6df4463901)




egrep '(^hello)' newfile 
## OUTPUT
![output]![output1_19](https://github.com/user-attachments/assets/9b8f78fe-3d2d-4993-bc06-0c46a627a70a)



egrep '(world$)' newfile 
## OUTPUT
![output]![output1_20](https://github.com/user-attachments/assets/397678d8-3b28-45d5-8205-230297ad5bb3)



egrep '(World$)' newfile 
## OUTPUT
![output](./output1_21.png)

egrep '((W|w)orld$)' newfile 
## OUTPUT
![output](./output1_22.png)


egrep '[1-9]' newfile 
## OUTPUT
![output](./output1_23.png)


egrep 'Linux.*world' newfile 
## OUTPUT
![output](./output1_24.png)

egrep 'Linux.*World' newfile 
## OUTPUT
![output](./output1_25.png)

egrep l{2} newfile
## OUTPUT
![output](./output1_26.png)


egrep 's{1,2}' newfile
## OUTPUT 
![output](./output1_27.png)

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
![output](./output1_28.png)


sed -n -e '$p' file23
## OUTPUT
![output](./output1_29.png)


sed  -e 's/Ram/Sita/' file23
## OUTPUT
![output](./output1_30.png)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![output](./output1_31.png)


sed  '/tom/s/5000/6000/' file23
## OUTPUT
![output](./output1_32.png)


sed -n -e '1,5p' file23
## OUTPUT
![output](./output1_33.png)


sed -n -e '2,/Joe/p' file23
## OUTPUT
![output](./output1_34.png)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![output](./output1_35.png)


seq 10 
## OUTPUT
![output](./output1_36.png)


seq 10 | sed -n '4,6p'
## OUTPUT
![output](./output1_37.png)


seq 10 | sed -n '2,~4p'
## OUTPUT
![output](./output1_38.png)


seq 3 | sed '2a hello'
## OUTPUT
![output](./output1_39.png)


seq 2 | sed '2i hello'
## OUTPUT
![output](./output1_40.png)

seq 10 | sed '2,9c hello'
## OUTPUT
![output](./output1_41.png)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![output](./output1_42.png)


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![output](./output1_43.png)
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
![output](./output1_44.png)

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
![output](./output1_45.png)


# Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![output](./output1_46.png)
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
![output](./output1_47.png)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![output](./output1_48.png)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
![output](./output1_49.png)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![output](./output1_50.png)

tar -xvf backup.tar
## OUTPUT
![output](./output1_51.png)
gzip backup.tar

ls .gz
## OUTPUT
 ![output](./output1_52.png)
gunzip backup.tar.gz
## OUTPUT
![output](./output1_53.png)
 
# Shell Script

echo '#!/bin/sh' > my-script.sh

echo 'echo Hello World‘; exit 0 >> my-script.sh

chmod 755 my-script.sh

./my-script.sh
## OUTPUT
![output](./output1_54.png)
 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![output](./output1_55.png)

cat < scriptest.sh 
```
bash
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
```
bash
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
![output](./output1_56.png)
 
ls file1
## OUTPUT
![output](./output1_57.png)
echo $?
## OUTPUT 
![output](./output1_58.png)
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![output](./output1_59.png)
abcd
 
echo $?
 ## OUTPUT
![output](./output1_60.png)

 
# mis-using string comparisons

cat < strcomp.sh 
```
bash
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
```
bash
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
![output](./output1_61.png)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![output](./output1_62.png)

# check file ownership
cat < psswdperm.sh 
```
bash
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
```
bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
```
 chmod 755 psswdperm.sh

./psswdperm.sh
## OUTPUT
![output](./output1_63.png)
# check if with file location
cat>ifnested.sh 
```
bash
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
chmod 755 ifnested.sh

./ifnested.sh 
## OUTPUT
![output](./output1_64.png)


# using numeric test comparisons
cat > iftest.sh 
```
bash
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
```
bash
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
![output](./output1_65.png)
# check if a file
cat > ifnested.sh
``` 
bash
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
bash
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
![output](./output1_66.png)
# looking for a possible value using elif
cat elifcheck.sh 
```
bash
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
![output](./output1_67.png)

# testing compound comparisons
cat> ifcompound.sh 
```
bash
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
![output](./output1_68.png)
# using the case command
cat >casecheck.sh 
```
bash
case $USER in Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";Rahim)
echo "Special testing account";gganesh)
echo "$USER, Do not forget to log off when you're done";*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
## OUTPUT
![output](./output1_69.png)

cat > whiletest.sh
```
bash
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
![output](./output1_70.png)
 
cat > untiltest.sh 
```
bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
```
$ chmod 755 untiltest.sh

$ ./untiltest.sh
 ## OUTPUT
 ![output](./output1_71.png)
cat forin1.sh 
```
bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
 
$ chmod 755 forin1.sh

$ ./forin1.sh
## OUTPUT
![output](./output1_72.png)
cat forin2.sh
``` 
bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
```
bash
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
![output](./output1_73.png)
cat forin3.sh 
```
bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
## OUTPUT
![output](./output1_74.png)

cat forin1.sh 
```
bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

cat forinfile.sh 
```
bash
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
```
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam
```
cat forctype.sh 
```
bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
```
$ chmod 755 forctype.sh

$ ./forctype.sh 

## OUTPUT
![output](./output1_75.png)

cat forctype1.sh 
```
bash
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
![output](./output1_76.png)

cat fornested1.sh
``` 
bash
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
![output](./output1_77.png)
 
cat forbreak.sh 
```
bash
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
![output](./output1_78.png)

cat forbreak.sh
``` 
bash
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
 
cat exread.sh 
```
bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT
![output](./output1_79.png)

 cat exread1.sh
```
bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program."
```
$ chmod 755 exread1.sh 

$ ./exread1.sh
## OUTPUT
![output](./output1_80.png)

 
cat funcex.sh
```
bash
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

 ## OUTPUT
![output](./output1_81.png)

 
 ./funcex.sh 1 2

## OUTPUT
![output](./output1_82.png)
 
cat argshift.sh
```
bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

$ ./argshift.sh 1 2 3
## OUTPUT
![output](./output1_83.png)

 cat argshift1.sh
```
bash
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
![output](./output1_84.png)

cat argshift.sh
```
bash
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
 ![output](./output1_85.png)

cat > nc.awk
```
bash
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
```
bash
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
 ![output](./output1_86.png)

cat > palindrome.sh
```
bash
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

chmod 755 palindrome.sh

./palindrome.sh
## OUTPUT 
![output](./output1_87.png)

# RESULT:
The Commands are executed successfully.

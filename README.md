### OS-Linux-commands-Shell-script
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

chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d

cat > file2

anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d

### Display the content of the files
cat < file1
## OUTPUT
![Screenshot from 2025-03-03 18-27-30](https://github.com/user-attachments/assets/fc3fd375-f574-45f9-aa8a-ddb38967ea85)

chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty



cat < file2
## OUTPUT
![Screenshot from 2025-03-03 18-28-12](https://github.com/user-attachments/assets/47c4fa9f-bf42-4522-b294-e4e0b640793f)

anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta



# Comparing Files
cmp file1 file2
## OUTPUT
![Screenshot from 2025-03-03 18-28-47](https://github.com/user-attachments/assets/28fa9e9a-3bd3-487e-9302-7472e12cbd7a)


file1 file2 differ: char1,line1
comm file1 file2

 
comm file1 file2
 ## OUTPUT
 ![Screenshot from 2025-03-03 18-29-18](https://github.com/user-attachments/assets/b93dc98b-da65-42f8-8518-03ec2acb0beb)

 
anil aggarwal
barun sengupta
c.k. shukla
chanchal singhvi
c.k. shukla
lalit chowdury
s.n. dasgupta


 
diff file1 file2
## OUTPUT
![Screenshot from 2025-03-03 18-29-43](https://github.com/user-attachments/assets/37a0a55d-9adf-44d6-b3c3-11d3ade10a5f)


--- file1
+++ file2
@@ -1,4 +1,5 @@
-chanchal singhvi
+anil aggarwal
+barun sengupta
 c.k. shukla
+lalit chowdury
 s.n. dasgupta
-sumit chakrobarty



#Filters

### Create the following files file11, file22 as follows:

cat > file11

Hello world
This is my world
^d

cat > file22

1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d



cut -c1-3 file11
## OUTPUT
![Screenshot from 2025-03-03 18-32-11](https://github.com/user-attachments/assets/5c4d7e20-173d-40a3-9f08-a4f5ea40caaa)


Hel
Thi




cut -d "|" -f 1 file22
## OUTPUT
![Screenshot from 2025-03-03 18-33-16](https://github.com/user-attachments/assets/b88300d9-ab44-42fa-8e04-54fd74b895b8)


1001
1002
1003




cut -d "|" -f 2 file22
## OUTPUT
![Screenshot from 2025-03-03 18-33-46](https://github.com/user-attachments/assets/1fdd2df0-d569-4e05-b01c-cfb183729fd3)


Ram
tom
Joe



cat < newfile 

Hello world
hello world
^d
`
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
![Screenshot from 2025-03-03 18-40-29](https://github.com/user-attachments/assets/917b9ffc-3be5-432b-9589-4a1a7fe4c56e)


Hello world



grep hello newfile 
## OUTPUT
![Screenshot from 2025-03-03 18-40-29 (copy)](https://github.com/user-attachments/assets/ef381929-d257-4b0c-8e0c-252330c29eb9)


Hello world




grep -v hello newfile 
## OUTPUT
![Screenshot from 2025-03-03 18-41-27](https://github.com/user-attachments/assets/144407e3-ae22-4d62-8552-849ef834170a)


Hello world




cat newfile | grep -i "hello"
## OUTPUT
![Screenshot from 2025-03-03 18-42-13](https://github.com/user-attachments/assets/7be111ab-d26b-41dd-9fcc-e229729d24bd)


Hello world
hello world




cat newfile | grep -i -c "hello"
## OUTPUT
![Screenshot from 2025-03-03 18-42-58](https://github.com/user-attachments/assets/043bc651-e72d-4931-871a-9bab4fc0872c)


2





grep -R ubuntu /etc
## OUTPUT
![Screenshot from 2025-03-03 18-44-53](https://github.com/user-attachments/assets/f08e4d7e-0332-4a6e-a8c2-45e9ae1806cc)


grep: unrecognized option: R
BusyBox v1.31.1 () multi-call binary.
 
Usage: grep [-HhnlLoqvsriwFE] [-m N] [-A/B/C N] PATTERN/-e PATTERN.../-f FILE [F
ILE]...
 
Search for PATTERN in FILEs (or stdin)
 
        -H      Add 'filename:' prefix
        -h      Do not add 'filename:' prefix
        -n      Add 'line_no:' prefix
        -l      Show only names of files that match
        -L      Show only names of files that don't match
        -c      Show only count of matching lines
        -o      Show only the matching part of line
        -q      Quiet. Return 0 if PATTERN is found, 1 otherwise
        -v      Select non-matching lines
        -s      Suppress open and read errors
        -r      Recurse
        -i      Ignore case
        -w      Match whole words only
        -x      Match whole lines only
        -F      PATTERN is a literal (not regexp)
        -E      PATTERN is an extended regexp
        -m N    Match up to N times per file
        -A N    Print N lines of trailing context
        -B N    Print N lines of leading context
        -C N    Same as '-A N -B N'
        -e PTRN Pattern to match
        -f FILE Read pattern from file




grep -w -n world newfile   
## OUTPUT
![Screenshot from 2025-03-03 18-45-54](https://github.com/user-attachments/assets/63087e1b-2915-49d7-8028-d9bb0649f90c)


1:Hello world
2:hello world



cat < newfile 

Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d


cat > newfile

Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 
egrep -w 'Hello|hello' newfile 
## OUTPUT
![Screenshot from 2025-03-03 18-47-41](https://github.com/user-attachments/assets/9cf7a6d0-56b4-4c7c-90eb-76b738b482da)


Hello world
hello world




egrep -w '(H|h)ello' newfile 
## OUTPUT
![Screenshot from 2025-03-03 18-50-28](https://github.com/user-attachments/assets/822e29ac-19c3-49a6-911e-e8fbefdbcc4f)


Hello world
hello world




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![Screenshot from 2025-03-03 18-51-19](https://github.com/user-attachments/assets/0cce5f96-d8f0-47f4-bc19-de834a0c338d)


Hello world
hello world





egrep '(^hello)' newfile 
## OUTPUT
![Screenshot from 2025-03-03 18-52-09](https://github.com/user-attachments/assets/e3432065-03a9-433e-be8a-1c249b8bcc31)


hello world



egrep '(world$)' newfile 
## OUTPUT
![Screenshot from 2025-03-03 18-52-45](https://github.com/user-attachments/assets/b92b2154-3421-4ba5-86fc-e27c1a148f15)


hello world
hello world



egrep '(World$)' newfile 
## OUTPUT
![Screenshot from 2025-03-03 18-53-27](https://github.com/user-attachments/assets/8bb673b8-5292-4e82-9120-6758aa2b13d5)


Linux is best in the World



egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot from 2025-03-03 20-59-06](https://github.com/user-attachments/assets/4121998e-1ee6-4efd-a99e-9028e885de36)


Hello world
hello world
Linux is best in this World




egrep '[1-9]' newfile 
## OUTPUT
![Screenshot from 2025-03-03 22-00-48](https://github.com/user-attachments/assets/8ec14413-49e0-4c8e-be22-ed14bd80b33b)


Linux is world number 1




egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2025-03-03 22-16-48](https://github.com/user-attachments/assets/99f80032-fe96-49f7-8002-cef8fe22c746)


Linux is world number 1



egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot from 2025-03-03 22-17-38](https://github.com/user-attachments/assets/d2717875-4a17-48f1-842e-d31715b7481f)


Linux is best in this World



egrep l{2} newfile
## OUTPUT
![Screenshot from 2025-03-03 22-18-57](https://github.com/user-attachments/assets/69aab01e-d0f5-4ac9-9415-2159f8544fb6)


Hello world
hello world




egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot from 2025-03-03 22-19-59](https://github.com/user-attachments/assets/28ec672c-8567-4444-b77a-e2a934a4b782)


Unix is predecessor
Linux is best in this World



cat > file23

1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d



sed -n -e '3p' file23
## OUTPUT
![Screenshot from 2025-03-03 22-26-52](https://github.com/user-attachments/assets/0429a541-7f13-4d89-b7d2-e71848e50a3f)


1002 | tom | 5000 | Admin




sed -n -e '$p' file23
## OUTPUT
![Screenshot from 2025-03-03 22-28-52](https://github.com/user-attachments/assets/e68afe49-b9f7-4bdd-87f4-cfc591d757d0)


1001 | Ram | 10000 | HR




sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2025-03-03 22-30-30](https://github.com/user-attachments/assets/561553b8-bc0f-44b0-8ce7-c1913d0e5047)


1001 | Sita | 10000 | HR
1001 | Sita | 10000 | HR
1002 | tom | 5000 | Admin
1003 | Joe | 7000 | Developer
1005 | Sam | 5000 | HR
1004 | Sit | 7000 | Dev
1003 | Joe | 7000 | Developer
1001 | Sita | 10000 | HR




sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2025-03-03 22-31-40](https://github.com/user-attachments/assets/5dc0ca5d-b884-4ee1-98cb-e0e1c7204908)


1001 | Ram | 10000 | HR
1001 | Sita | 10000 | HR
1002 | tom | 5000 | Admin
1003 | Joe | 7000 | Developer
1005 | Sam | 5000 | HR
1004 | Sit | 7000 | Dev
1003 | Joe | 7000 | Developer
1001 | Ram | 10000 | HR




sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot from 2025-03-03 22-32-44](https://github.com/user-attachments/assets/a6a7e0be-8294-4729-be26-24965e2df4b7)


1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom | 6000 | Admin
1003 | Joe | 7000 | Developer
1005 | Sam | 5000 | HR
1004 | Sit | 7000 | Dev
1003 | Joe | 7000 | Developer
1001 | Ram | 10000 | HR




sed -n -e '1,5p' file23
## OUTPUT
![Screenshot from 2025-03-03 22-33-49](https://github.com/user-attachments/assets/7e4f6404-9c23-48d6-9a0b-87a520c5c0bb)


1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom | 5000 | Admin
1003 | Joe | 7000 | Developer
1005 | Sam | 5000 | HR



sed -n -e '2,/Joe/p' file23
## OUTPUT
![Screenshot from 2025-03-03 22-33-49](https://github.com/user-attachments/assets/1842665e-79fd-4584-a1ff-4a598fac8c5e)

1001 | Ram | 10000 | HR
1002 | tom | 5000 | Admin
1003 | Joe | 7000 | Developer





sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Screenshot from 2025-03-03 22-35-24](https://github.com/user-attachments/assets/1c934f9f-6d3a-4a32-b65b-31f78e2b8d7a)


1002 | tom | 5000 | Admin
1003 | Joe | 7000 | Developer




seq 10 
## OUTPUT
![Screenshot from 2025-03-03 22-35-52](https://github.com/user-attachments/assets/6c715fd8-e4ef-447f-92cc-cec4ae2d1e3a)


1
2
3
4
5
6
7
8
9
10




seq 10 | sed -n '4,6p'
## OUTPUT
![Screenshot from 2025-03-03 22-36-33](https://github.com/user-attachments/assets/ae951d5e-71a0-4ea4-9760-17ad880643e5)


4
5
6




seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot from 2025-03-03 22-37-07](https://github.com/user-attachments/assets/035e2abc-1f21-44dd-a5c4-bdbdf13be9d7)


2
3
4




seq 3 | sed '2a hello'
## OUTPUT
![Screenshot from 2025-03-03 22-37-38](https://github.com/user-attachments/assets/1c0053a2-95eb-435b-a143-229fbc4482e8)


1
2
hello
3




seq 2 | sed '2i hello'
## OUTPUT
![Screenshot from 2025-03-03 22-38-02](https://github.com/user-attachments/assets/b72c6c02-e09d-4a1e-936f-6773b0a557d3)


1
hello
2



seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot from 2025-03-03 22-38-36](https://github.com/user-attachments/assets/39e66117-4b7f-4aff-bf07-33ca9d109718)


1
hello
10




sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![Screenshot from 2025-03-03 22-39-45](https://github.com/user-attachments/assets/c310bca8-00c3-4f03-9560-901183c31fb9)


$1001 | Ram | 10000 | HR
$1002 | tom | 5000 | Admin
$1003 | Joe | 7000 | Developer




sed -n '2,4{s/$/*/;p}' file23

##ouput 
![Screenshot from 2025-03-03 22-40-29](https://github.com/user-attachments/assets/d0a3afd6-893c-4b48-a20a-cd70b33c5d2d)


1001 | Ram | 10000 | HR*
1002 | tom |  5000 | Admin*
1003 | Joe |  7000 | Developer*

#Sorting File content
cat > file21

1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
 
sort file21
## OUTPUT
![Screenshot from 2025-03-03 22-43-46](https://github.com/user-attachments/assets/56cf6b79-ec4e-4803-bf46-62d0a1ad880a)


1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1004 | Sit |  7000 | Dev
1005 | Sam |  5000 | HR



cat > file22

1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
 
uniq file22
## OUTPUT
![Screenshot from 2025-03-03 22-46-13](https://github.com/user-attachments/assets/e521ad0a-7e1a-4088-9e15-8bebbec2f829)


1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 ![Screenshot from 2025-03-03 22-47-30](https://github.com/user-attachments/assets/a3d01fc8-644f-4499-a4da-acaabe53b38d)


1001 | RAM | 10000 | HR
1001 | RAM | 10000 | HR
1002 | TOM |  5000 | ADMIN
1003 | JOE |  7000 | DEVELOPER
1005 | SAM |  5000 | HR
1004 | SIT |  7000 | DEV
1003 | JOE |  7000 | DEVELOPER
1001 | RAM | 10000 | HR

cat < urllist.txt

www. yahoo. com
www. google. com
www. mrcet.... com
^d
 
cat > urllist.txt

www. yahoo. com
www. google. com
www. mrcet.... com
 
cat urllist.txt | tr -d ' '
 ## OUTPUT
 ![Screenshot from 2025-03-03 22-54-40](https://github.com/user-attachments/assets/79b4143c-9787-4f7e-9fcd-e34fe130c4e3)


www.yahoo.com
www.google.com
www.mrcet....com


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![Screenshot from 2025-03-03 22-56-51](https://github.com/user-attachments/assets/cfff961d-8621-429c-bb32-556217e7eba4)


www.yahoo.com
www.google.com
www.mrcet.com



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![Screenshot from 2025-03-03 23-01-49](https://github.com/user-attachments/assets/d6245cce-820a-4541-bfe9-521150d21599)


bench.py
file1
file11
file2
file21
file22
file23
hello.c
hello.js
newfile
readme.txt
urllist.txt



mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![Screenshot from 2025-03-03 23-11-15](https://github.com/user-attachments/assets/af4e1210-2b36-44c4-bf25-ece46103c45e)


drwxr-xr-x root/root         0 2024-08-16 10:12:02 backupdir/
-rw-r--r-- root/root     13312 2024-08-16 10:10:04 backupdir/backup.tar
-rw-r--r-- root/root       114 2020-07-05 23:17:07 bench.py
-rw-r--r-- root/root        61 2024-08-16 09:48:52 file1
-rw-r--r-- root/root        29 2024-08-16 09:52:03 file11
-rw-r--r-- root/root        70 2024-08-16 09:49:11 file2
-rw-r--r-- root/root       131 2024-08-16 10:06:47 file21
-rw-r--r-- root/root       155 2024-08-16 10:07:30 file22
-rw-r--r-- root/root       210 2024-08-16 10:02:59 file23
-rw-r--r-- root/root        76 2020-07-03 14:45:56 hello.c
-rw-r--r-- root/root        22 2020-06-26 14:57:33 hello.js
-rw-r--r-- root/root        96 2024-08-16 09:57:21 newfile
-rw-r--r-- root/root       151 2020-07-05 23:19:13 readme.txt
-rw-r--r-- root/root        52 2024-08-16 10:09:28 urllist.txt



tar -xvf backup.tar
## OUTPUT
![Screenshot from 2025-03-03 23-11-33](https://github.com/user-attachments/assets/f4c892c6-f8b7-41f8-97ae-9ef96fea1c0c)


backupdir/
backupdir/backup.tar
bench.py
file1
file11
file2
file21
file22
file23
hello.c
hello.js
newfile
readme.txt
urllist.txt

gzip backup.tar

ls .gz
## OUTPUT
![Screenshot from 2025-03-03 23-12-01](https://github.com/user-attachments/assets/fc2a783f-8c56-47a6-b67c-a00691221aae)

 
gunzip backup.tar.gz
## OUTPUT
![Screenshot from 2025-03-03 23-20-01](https://github.com/user-attachments/assets/433d7289-3505-4600-a8c6-5cb5d4fca698)
 
# Shell Script

echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh

chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![Screenshot from 2025-03-03 23-36-59](https://github.com/user-attachments/assets/80d7e29f-3c97-430d-8b44-93c7795402b9)
 
cat << stop > herecheck.txt

hello in this world
i cant stop
for this non stop movement
stop


cat herecheck.txt
## OUTPUT
![Screenshot from 2025-03-03 23-42-28](https://github.com/user-attachments/assets/f1a27a90-42df-46f6-8e0f-3dbc8faa4a20)


hello in this world
i cant stop
for this non stop movement



cat < scriptest.sh 
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
 

cat scriptest.sh 

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

 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
![Screenshot from 2025-03-03 23-42-55](https://github.com/user-attachments/assets/e22e728b-09ab-4a30-987c-d2b46defb6c3)


./scriptest.sh: line 1: #!/bin/sh: not found
“File name is ./scriptest.sh ”
File name is  scriptest.sh
“First arg. is ” 1
“Second arg. is ” 2
“Third arg. is ” 3
“Fourth arg. is ”
The $@ is  1 2 3
The $\# is  1#
The $$ is  200
PID   USER     TIME  COMMAND
    1 root      0:01 {init} /bin/sh /sbin/init
    2 root      0:00 [kthreadd]
    3 root      0:00 [kworker/0:0]
    4 root      0:00 [kworker/0:0H]
    5 root      0:00 [kworker/u2:0]
    6 root      0:00 [mm_percpu_wq]
    7 root      0:00 [ksoftirqd/0]
    8 root      0:00 [kdevtmpfs]
    9 root      0:00 [oom_reaper]
   10 root      0:00 [writeback]
   11 root      0:00 [kcompactd0]
   12 root      0:00 [crypto]
   13 root      0:00 [bioset]
   14 root      0:00 [kblockd]
   15 root      0:00 [kworker/0:1]
   16 root      0:00 [kswapd0]
   17 root      0:00 [bioset]
   34 root      0:00 [khvcd]
   35 root      0:00 [bioset]
   36 root      0:00 [bioset]
   37 root      0:00 [bioset]
   38 root      0:00 [bioset]
   39 root      0:00 [bioset]
   40 root      0:00 [bioset]
   41 root      0:00 [bioset]
   42 root      0:00 [bioset]
   55 root      0:00 settime -d /
   56 root      0:00 dhcpcd -q
   61 root      0:00 sh -l
   62 root      0:00 [kworker/u2:1]
  200 root      0:00 {busybox} ash ./scriptest.sh 1 2 3
  203 root      0:00 ps


 
ls file1
## OUTPUT
![Screenshot from 2025-03-03 23-43-46](https://github.com/user-attachments/assets/aba3205a-e0c8-47f7-9941-07f73f6edb12)


file1


echo $?
## OUTPUT 
![Screenshot from 2025-03-03 23-44-14](https://github.com/user-attachments/assets/d84167fc-cb50-43b2-ae39-45f093c1232f)


0

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![Screenshot from 2025-03-03 23-44-14](https://github.com/user-attachments/assets/ffb57b62-9fb5-4702-9c6d-c9860a385b68)


127
 
abcd
 
echo $?
 ## OUTPUT
![Screenshot from 2025-03-03 23-45-50](https://github.com/user-attachments/assets/16757fa1-afec-4afe-bdad-00f61f580ea5)


127

 
# mis-using string comparisons

cat < strcomp.sh 
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


cat strcomp.sh 
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





chmod 755 strcomp.sh
 
./strcomp.sh 

## OUTPUT
![Screenshot from 2025-03-04 07-03-03](https://github.com/user-attachments/assets/8e456423-7beb-4ac9-a892-8c2ebb8a32f4)


./strcomp.sh: line 1: #!/bin/bash: not found
baseball is less than hockey
./strcomp.sh: line 10: ^d: not found



# check file ownership
cat < psswdperm.sh 
bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d


cat psswdperm.sh 
bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 
./psswdperm.sh
## OUTPUT
![Screenshot from 2025-03-04 07-04-09](https://github.com/user-attachments/assets/179e2762-81cc-4bed-963a-a3dc42bd4d9d)


bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi


# check if with file location
cat>ifnested.sh 
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

cat ifnested.sh 

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


./ifnested.sh 

## OUTPUT
![Screenshot from 2025-03-04 07-05-08](https://github.com/user-attachments/assets/acaad9db-cc83-44bf-bb76-9ab2335ab57c)

sh: ./ifnested.sh: Permission denied



# using numeric test comparisons
cat > iftest.sh 
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



cat iftest.sh 
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


$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT
![Screenshot from 2025-03-04 07-06-01](https://github.com/user-attachments/assets/8c403da8-843a-4eec-a4e9-273fb213ce46)


# check if a file
cat > ifnested.sh 
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


cat ifnested.sh 
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


$ chmod 755 ifnested.sh
 
$ ./ifnested.sh ##OUTPUT

# looking for a possible value using elif
cat elifcheck.sh 
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


$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 

## OUTPUT
![Screenshot from 2025-03-04 07-06-56](https://github.com/user-attachments/assets/97210ed0-b7e5-4310-9f62-f08fbd4f3918)

# testing compound comparisons
cat> ifcompound.sh 
bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi

$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
![Screenshot from 2025-03-04 07-07-18](https://github.com/user-attachments/assets/92a5282c-08ac-4bc6-8555-60d5535dbb48)

# using the case command
cat >casecheck.sh 
bash
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

$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 ![Screenshot from 2025-03-04 07-07-56](https://github.com/user-attachments/assets/e7fc7408-35f6-476f-ba83-98771e24d6bc)

cat > whiletest
![Screenshot from 2025-03-04 07-09-09](https://github.com/user-attachments/assets/db951484-1386-49dc-be11-e27eedd6fe44)

bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done

$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
![Screenshot from 2025-03-04 07-07-56](https://github.com/user-attachments/assets/360346dd-6149-4d59-86b4-22e048af9101)

!cat untiltest.sh 
bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
 
$ chmod 755 untiltest.sh
![Screenshot from 2025-03-04 07-09-32](https://github.com/user-attachments/assets/23b00b44-a962-46da-989b-6771149b9223)
 
cat forin1.sh 
![Screenshot from 2025-03-04 07-10-27](https://github.com/user-attachments/assets/2a509800-62ae-4708-8963-b55dc70fb074)

bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 
 
$ chmod 755 forin1.sh
 
 
cat forin2.sh 
![Screenshot from 2025-03-04 07-10-43](https://github.com/user-attachments/assets/8cb9caf5-ba4a-478e-a2b6-8907de84989a)

bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done

$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 ![Screenshot from 2025-03-04 07-10-43](https://github.com/user-attachments/assets/417a888f-983b-44f4-bd38-a0edd512cb9f)

cat forin3.sh 
bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done

$ ./forin3.sh 
 ![Screenshot from 2025-03-04 07-10-54](https://github.com/user-attachments/assets/bea565ed-3e60-4fa5-a923-a2252fd878d6)

cat forin1.sh 
bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done

$ chmod 755 forin1.sh

## OUTPUT

cat forinfile.sh 
bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done

$ chmod 777 forinfile.sh
![Screenshot from 2025-03-04 07-11-11](https://github.com/user-attachments/assets/22316a6f-9a79-4e8c-b309-aa186ccec983)

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
bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
`
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT
![Screenshot from 2025-03-04 07-11-38](https://github.com/user-attachments/assets/b4f16516-7f1e-4266-80e4-a89a6802e222)

cat forctype1.sh 
bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done

$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT
![Screenshot from 2025-03-04 07-11-45](https://github.com/user-attachments/assets/56bb29a9-e363-4afb-9f6e-2b09a9f20e5f)

cat fornested1.sh 
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

$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
 ![Screenshot from 2025-03-04 07-12-36](https://github.com/user-attachments/assets/8b51e43c-073a-46fc-bfa6-d405a1844ff9)
 
cat forbreak.sh 
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

## OUTPUT
![Screenshot from 2025-03-04 07-12-53](https://github.com/user-attachments/assets/a8e75390-3a09-4e8c-ac94-5ec62a12d5e0)

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
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


 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 ![Screenshot from 2025-03-04 07-13-13](https://github.com/user-attachments/assets/a379ce12-4ede-48b3-8230-c41f9171a3f2)

cat exread.sh 
bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT
![Screenshot from 2025-03-04 07-13-37](https://github.com/user-attachments/assets/6e39b304-7856-418b-a0cf-c5dadca1e896)

 cat exread1.sh
bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
 
$ chmod 755 exread1.sh 

## OUTPUT

![Screenshot from 2025-03-04 07-13-43](https://github.com/user-attachments/assets/f5c39456-f600-4d73-99e3-31e3410f4057)

$ ./exread1.sh 
 
cat funcex.sh
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

## OUTPUT
![Screenshot from 2025-03-04 07-13-58](https://github.com/user-attachments/assets/1cedb859-412c-46c5-ba4e-c18402f5e70e)

 ./funcex.sh 

 
 ./funcex.sh 1 2

 
cat argshift.sh
bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done

$ chmod 777 argshift.sh

## OUTPUT
![Screenshot from 2025-03-04 07-15-22](https://github.com/user-attachments/assets/470cc4ee-209f-45c8-a320-ef5c2829c405)

$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
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

$ chmod 777 argshift.sh
## OUTPUT
![Screenshot from 2025-03-04 07-15-34](https://github.com/user-attachments/assets/3276aedf-93e0-4c9c-aea9-2340e3f92565)

$ ./argshift.sh 1 2 3
 
cat argshift.sh
bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x

## OUTPUT
![Screenshot from 2025-03-04 07-15-57](https://github.com/user-attachments/assets/f45d5a76-4bc4-4b24-a299-225578c18079)


 ./argshift.sh 1 2 3
 
 
cat > nc.awk
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
 
cat>data.dat
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

awk -f nc.awk data.dat
## OUTPUT 
 ![Screenshot from 2025-03-04 07-16-17](https://github.com/user-attachments/assets/cc975b0d-a5b5-4028-a3c7-0fdee1eb7c30)

cat > palindrome.sh
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



![Screenshot from 2025-03-04 07-16-34](https://github.com/user-attachments/assets/936cfd69-62d4-4bee-975a-4dc801952a99)


# RESULT:
The Commands are executed successfully.

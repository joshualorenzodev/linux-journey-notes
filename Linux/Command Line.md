# 1. `echo` and The Shell
> The `echo` command prints out the text arguments to the display. #cmd

> The **shell** is a program that takes your command from keyboard and sends to the OS to perform.

```shell
echo Hello World
```
```txt
Hello World
```

> The `date` command outputs the current date. #cmd

```shell
date
```
```txt
Wed May 18 05:47:54 PM CDT 2022
```


> The `whoami` command outputs the current user logged in. #cmd

```shell
whoami
```
```txt
enzo
```


---

# 2. `pwd` (Print Working Directory)
> The `pwd` command shows which directory you are in. #cmd

- first directory in the filesystem is named `root` directory

```txt
/ 
|-- bin 
| |-- file1 
| |-- file2 
|-- etc 
| |-- file3 
| `-- directory1 
| |-- file4 
| `-- file5 
|-- home 
|-- var
```

```shell
pwd
```

```txt
/home/enzo
```

---

# 3. `cd` (Change Directory)
> The `cd` command will change the current directory. #cmd 

Two ways to specify a path
1. `Absolute` - path from the `root` directory
	- root is the highest directory
	- root is commonly shown as `/` (forward slash)
2. `Relative` - path from where you are currently in the file sys
	- don't need to specify the whole path from root
	- can just treat the current dir as the starting 'root'
	
Absolute Pathing	
```shell
cd /home/enzo/Pictures
```

Relative Pathing
```shell
cd Selfies
```

Shortcuts
- `.` - the **current** dir
- `..` - the **parent** dir
- `~` - the **home** dir `/home/enzo`
- `-` - the **previous** dir

---

# 4. `ls` (List Directory)
> The `ls` command lists the contents of the current directory. #cmd 

```shell
ls /home/enzo
```
```txt
Desktop  Documents  Downloads  Music  Pictures  Public  Templates  Videos
```

Options
- `-a` - includes the hidden files in a dir (hidden files are prefixed with a `.`)
- `-l` - shows a detailed list of files in a long format
-  These options can be used at the same time

```shell
ls -a
ls -l
ls -la
```

```txt
total 32
drwxr-xr-x 2 enzo enzo 4096 May 17 17:07 Desktop
drwxr-xr-x 2 enzo enzo 4096 May 17 17:07 Documents
drwxr-xr-x 2 enzo enzo 4096 May 17 17:07 Downloads
drwxr-xr-x 2 enzo enzo 4096 May 17 17:07 Music
drwxr-xr-x 2 enzo enzo 4096 May 17 17:07 Pictures
drwxr-xr-x 2 enzo enzo 4096 May 17 17:07 Public
drwxr-xr-x 2 enzo enzo 4096 May 17 17:07 Templates
drwxr-xr-x 2 enzo enzo 4096 May 17 17:07 Videos
```


---

# 5. `touch` command
> The `touch` command creates new empty files. #cmd 

```shell
mkdir Linux_Journey
cd Linux_Journey
touch newFile
ls
```

```txt
-rw-r--r-- 1 enzo enzo 0 May 18 18:23 newFile
```


---

# 6. `file` command
> The `file` command will output the file type of a file. #cmd 

```shell
file newFile
```

```txt
newFile: empty
```

```shell
file Linux_Journey
```

```txt
Linux_Journey: directory
```

---

# 7. `cat` command
> The `cat` command is short for *concatenate* and it outputs the contents of the file

- It not only displays file contents, but it can combine multiple files and show you the output of them
- It's not great for viewing large files and it's only meantfor short content

```shell
cat firstName.txt
```

```txt
Joshua
```

```shell
cat firstName.txt lastname.txt
```

```
JoshuaGarcia
```
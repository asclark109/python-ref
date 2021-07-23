# Test

### Errors
Syntax Error: related to syntax/structure of the program. program halts as soon as pythong parses program

Runtime Error: error that only occurs while program is running 

Semantic (Logical) Error: program runs but does not do what is expected

### Useful basic bash (UNIX shell) commands
'''bash
ls
cd
mv
mkdir
rmdir
man
touch
rm -i
clear
cp
which
whoami
'''

| Bash      | Description 
| :---        |    :----:   | 
| pwd	| print working directory |
| hostname	|my computer's network name|
| mkdir	|make directory|
| cd	|change directory|
| ls	|list directory|
| rmdir	|remove directory|
|rm -rf |	deletes it and all its contents
| pushd	|push directory|
| popd	|pop directory|
| cp	|copy a file or directory|
|cp -r |? copy file/directory and all its contents
| mv	|move a file or directory|
| less	|page through a file|
| cat	|print the whole file|
| xargs	|execute arguments|
| find	|find files|
| grep	|find things inside files|
| man	|read a manual page|
| apropos|	find which man page is appropriate|
| env	|look at your environment|
| echo	|print some arguments|
| export|	export/set a new environment variable|
| exit	|exit the shell|
| sudo	| DANGER! become super user root DANGER!|
| chmod |	change the access permissions of file system objects (files and directories) sometimes  known as modes |
|chown	| abbreviation of change owner, is used on Unix and Unix-like operating systems to change the owner of file system files, directories|
|tar	| https://www.howtogeek.com/248780/how-to-compress-and-extract-files-using-the-tar-command-on-linux/|

| Windows Shell | Description |
| :---        |    :----:   | 
|pwd	|print working directory|
|hostname	|my computer's network name
|mkdir	|make directory
|cd	|change directory
|ls	|list directory
|rmdir	|remove directory
|pushd	|push directory
|popd	|pop directory
|cp	|copy a file or directory
|robocopy|	robust copy
|mv	|move a file or directory
|more	|page through a file
|type	|print the whole file
|forfiles	|run a command on lots of files
|dir -r	|find files
|select-string|	find things inside files
|help	|read a manual page
|helpctr	|find what man page is appropriate
|echo	|print some arguments
|set	|export/set a new environment variable
|exit	|exit the shell
|runas	|DANGER! become super user root DANGER!

### Escape Characters
|Escape	|What it does|
| :---        |    :----:   | 
|\\	|Backslash (\)
|\’	|Single-quote (‘)
|\’’	|Double-quote (“)
|\a	|ASCII bell (BEL)
|\b	|ASCII backspace (BS)
|\f	|ASCII formfeed (FF)
|\n	|ASCII linefeed (LF)
|\N{name}	|Character named name in the Unicode database (Unicode only)
|\r	|Carriage return (CR)
|\t	|Horizontal tab (TAB)
|\uxxxx	|Character with 16-bit hex value xxxx
|\Uxxxxxxxx	|Character with 32-bit hex value xxxxxxxx
|\v	|ASCII vertical tab (VT)
|\000	|Character with octal value 000
|\xhh	|Character with hex value hh



```go
package main // a package must be defined
import "fmt"
func main() {
  fmt.Println("Hello World!")
}
```

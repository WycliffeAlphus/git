
## Git commits to commit
#### Create a work directory and hello subdirectory
```console
mkdir work
cd work
mkdir hello
cd hello
```
#### Create a file named hello.sh with content using the following command:
```console
echo "Hello, World" > hello.sh
```
#### Initialize the git repository in the hello directory:
```console
git init
```
#### I then checked the status: 
```console
git status
```
The output showed that I had untracked files: "hello.sh"
#### I used the following commands, that is staged and commited the file:
```console
git add hello.sh

git commit -m "feat:add hello.sh file"
```
#### Change the content of hello.sh
```console
nano hello.sh
```
I then staged the file and commited the changes. I also confirmed that the working tree is clean

I noticed that the branch name is master, therefore, I changed it to main using the command:
```
git branch -m master main
````
The following is the result of git status:

![](status.png)
#### I changed the content for the second time


I used the following command to check the changes:
```console
git diff hello.sh
```
I then staged the changes interatively to commit specific lines separately using the following command:
```console
git add -p hello.sh
````
The prompt below will appear:
```
Stage this hunk [y,n,q,a,d,e,?]? 
```
Choose 'e' to edit the chunk manually

I deleted the sections that I did not want to include in the first commit.
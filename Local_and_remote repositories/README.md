### Clone Repository

Use the command:

```console
git clone hello hello_clone
```
![](clone.png)

### Show logs for hello_clone

![](log.png)

### Display the name of the remote repository 

```console
git remote
```

![](name1.png)

To get detailed information:

```console
git remote -v
```

![](name.png)

### List all remote and local branches in the cloned_hello repository.

```console
git branch -a
```
![](all.png)

### I made changes to original repository and updated the README.md file with the provided content, and commited the changes.

![](changes.png)

### In the cloned_hello, I fetched the changes from the remote repository and displayed the logs.

![](clo.png)

### Merge the changes from the remote main branch into the local main branch.

![](merge.png)

### Add a local branch named greet tracking the remote origin/greet branch.

```console
git checkout -b greet origin/greet
```
![](image.png)

### Add a remote to your Git repository and push the main and greet branches to the remote.

To add a remote use:

```console
git remote add origin <url>
```
However the command led to an error indicating that origin already exists, therefore I used:

```console
git remote set-url origin <url>
```
![](set.png)

To push main:

```console
git push -u origin main
```
To push greet:

```console
git push -u origin greet
```
![](push.png)

**The single git command equivalent to what was done with the fetching and merging changes from remote to local main branch is:**

```console
git pull
```

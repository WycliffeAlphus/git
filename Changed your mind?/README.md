## Changed your mind?
#### Reverting changes
I made changes to the file

I then went ahead and restored the file to the way it was before the changes using:

```console
git restore hello.sh
```

![](change.png)


#### Staging and Cleaning:

I then introduced unwanted changes to the file

I staged them and then cleaned the staging area to discard the changes:
```console
git restore --staged hello.sh
```
![](unstage.png)

I then added unwanted changes again, staged the file and committed the changes

Thereafter, I reverted them back to their original state:
```console
git revert HEAD
```
If nano opens: Just press Ctrl+X and the reverting will be completed

![](revert.png)

#### Tagging and Removing Commits: 

I tagged the latest commit with oops

![](tagoops.png)

I then reset to v1:
```console
git reset --hard v1
```
The commits made after the v1 version will be removed 

![](deleteabovev1.png)

I also checked out v1 to ensure head is at v1:

![](checkoutv1.png)

#### Displaying Logs with Deleted Commits: 
Use: 
```console
git reflog
```
![](reflog.png)

To be more specific and get the commit tagged oops:

```console
git show oops
```
![](gitshow.png)

#### Cleaning Unreferenced Commits: 

To delete unreferenced commits from history use:
```console
git gc --prune=now
```
![](prune.png)

However, after running 'git reflog' I noticed that the commit history with oops still exists.

I therefore used :
```console
git reflog delete HEAD@{2}
```
![](reflogdelete.png)

After ensuring that I have deleted the commits that came after v1, below is the result:

![](delref.png)

#### Author Information: 

I then made changes to the file to include author name and committed the changes:

![](author.png)

##### To add the email of the author without adding a new commit:

First stage the changes and run the command:

```console
git commit --amend --no-edit
```
![](del.png)
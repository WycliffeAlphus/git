## Create and Switch to New Branch: 

To creat a local branch named greet and switch to it use:

```console
git checkout -b greet
```
I then created a file named greeter.sh:

![](greet.png)

I then updated the hello.sh file:

![](update.png)

I also updated the Makefile:

![](MkUp.png)

Switch back to the main branch, compare and show the differences between the main and greet:
Use:

```console
git diff greet
```
![](diff.png)

I then added a README.md and committed it:

![](RD.png)

Drawing of diverging changes

![](<WhatsApp Image 2024-07-10 at 11.22.49.jpeg>)
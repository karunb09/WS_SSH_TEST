# Using Git Successfully (SSH, Merge Conflicts, incremental commits, continuous integration)

# Team-Members

1. Karun Bourishetty
2. Aawaj Joshi
3. Dristi Marasini
4. Sirisha Devineni


# Repo link
https://github.com/karunb09/WS_SSH_TEST


# Team Slide
![teamslide](https://github.com/karunb09/WS_SSH_TEST/blob/master/Capture.PNG)


## Requirements

1. PuttyGen (download here http://www.puttygen.com
2. GitHub Account


# Link to view Presentation

https://docs.google.com/presentation/d/1RRZ3ZxW62gY6JiTtrdh-XzICVqXQvs4f5gHKWr3DToQ/edit?usp=sharing

# Account in github

---

# Steps to follow in order to set up SSH.

1. we generate RSA public and private key using PUTTY-Gen.
2. Enter a new passphrase which is of your choice, reenter the same in the next input.(which will be used while pulling or pushing the repo).
3. save the private key in C:\Users\(your_systemname)\.ssh (if there isnt any folder create a new folder using touch command in gitbash).
4. login to your Github --> direct to settings --> click on SSH and GPG keys
5. you can find add key button, click on it and enter the label as required and paste the public key which you have generated using puttyGen
6. when pushing the repo into the cloud or while pulling the repo, in the dialogue box we can see an input field called putty key or load puttyKey(browse through the fileexplorer and select the key which you have created).
7. After we click on, we get a dialogue box, where it asks for the passphrase, enter the same where you filled in puttygen.
8. All done .. !!!! , the server will not ask for login details instead a passphrase is been asked.

---

# Merge Conflicts

```C#
CONFLICT (content): Merge conflict in README.md
CONFLICT (content): Merge conflict in Program.cs
Automatic merge failed; fix conflicts and then commit the result.
```
Merge conflicts can arise due a number of different reasons. The two most common instances when a merge conflict can happen is when two contributors edit the same lines of the same file and when one contributor deletes a file that the other has modified. 

As scary as they might sound, most cases of merge conflict can be resolved with ease. Here is a list of steps to resolve a merge conflict occured as a result of two contributors editing the same lines in a file.

1. First, understand what happened. ```git status``` enables user to generate a list of files that need to be resolved.  

2. Git encloses problematic areas in a file within conflict markers separated by a divide.   
```
<<<<<<< HEAD(master)
conflicted text from HEAD(master)
=======
conflicted text from hotfix
>>>>>>> hotfix
```  
Here, contents after the first marker ```<<<<<<< HEAD(master)```, ```conflicted text from HEAD(master)``` originates from the user's current working branch. ```=======``` separates your changes from the changes in other branch.  

3. The user can then consult his/her/their teammates and decide which code to keep.  

4. Next, delete the conflict markers and divides as well as the unnecessary code.  

5. User can then commit changes with ```git commit``` to generate the merge commit.  

---

# Incremental commits

1. The main purpose of using source control system is to keep track of changes.
In git these are called commits.

2. We should always commit early and often.

3. In commit process, we should include useful commit messages.

# references

https://help.github.com/articles/connecting-to-github-with-ssh/






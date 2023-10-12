1) 

    > cat file.txt  
    1
    

<hr>

2) 
    

    > echo 2 > file.txt

<hr>

3)  

    diff --git a/file.txt b/file.txt
    index ca90535..c7250cb 100644
    Binary files a/file.txt and b/file.txt differ

<hr>

4) empty, because we didn't add the changes yet.

<hr>
5) 

    > git add file.txt

<hr>

6) empty.

<hr>

7) 

    diff --git a/file.txt b/file.txt
    index ca90535..c7250cb 100644
    Binary files a/file.txt and b/file.txt differ

<hr>

8) 

    > echo 3 > file.txt

<hr>

9)

    diff --git a/file.txt b/file.txt
    index c7250cb..00b30ed 100644
    Binary files a/file.txt and b/file.txt differ

<hr>

10) 

    diff --git a/file.txt b/file.txt
    index ca90535..c7250cb 100644
    Binary files a/file.txt and b/file.txt differ

<hr>

11) In the first overwriting then adding changes, this first overwrite become staged, and no changes were in working directory, untill we reach the 8th point, there we did a new change to work directory, but this change won't affect the staged changes.

<hr>

12) 

    On branch master
    Changes to be committed:
      (use "git restore --staged <file>..." to unstage)
            modified:   file.txt
    
    Changes not staged for commit:
      (use "git add <file>..." to update what will be committed)
      (use "git restore <file>..." to discard changes in working directory)
            modified:   file.txt

<hr>

13) 

    > git restore --staged file.txt

<hr>

14) 

    On branch master
    Changes not staged for commit:
      (use "git add <file>..." to update what will be committed)
      (use "git restore <file>..." to discard changes in working directory)
            modified:   file.txt
<hr>

15) 

    > git add file.txt
    > git commit -m "file.txt overrided"

<hr>

16) 

    commit 65f5d9c77690a3401682d9b06b8aa1b996b0cd83 (HEAD -> master)
    Author: Ayman Attili <a.l.ateeli@students.ptuk.edu.ps>
    Date:   Thu Oct 12 22:39:43 2023 +0300
    
        file.txt overrided

<hr>

17) 

    > echo 4 > file.txt

<hr>

18)

    > cat file.txt -> 4

<hr>

19)

    On branch master
    Changes not staged for commit:
      (use "git add <file>..." to update what will be committed)
      (use "git restore <file>..." to discard changes in working directory)
            modified:   file.txt
    
    no changes added to commit (use "git add" and/or "git commit -a")

<hr>

20) 

    > git restore file.txt

<hr>

21) 

    > cat file.txt  
    3

<hr>

22) 

    On branch master
    nothing to commit, working tree clean

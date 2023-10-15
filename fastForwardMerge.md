1) 

    >  git branch feature/uppercase  
    

<hr>

2) 
    

    > git checkout feature/uppercase

<hr>

3)  

    On branch feature/uppercase
    nothing to commit, working tree clean

<hr>

4) 

    > echo HELLO > greeting.txt

<hr>

5) 

    > git add greeting.txt
    > git commit -m 'greeting edited'

<hr>

6) 

    * feature/uppercase
    master

<hr>

7) 

    * 6dfc739 (HEAD -> feature/uppercase) greeting edited
    * 7d6acd3 Add content to greeting.txt
    * 4230ce0 Add file greeting.txt

<hr>

8) 

    > git checkout master

<hr>

9)

    > cat greeting.txt

<hr>

10) 

    > git diff master feature/uppercase
    diff --git a/greeting.txt b/greeting.txt
    index ce01362..0d7de81 100644
    Binary files a/greeting.txt and b/greeting.txt differ


<hr>

11) 

    > git merge feature/uppercase


<hr>

12) 

    > cat greeting.txt

<hr>

13) 

    > git branch -d feature/uppercase

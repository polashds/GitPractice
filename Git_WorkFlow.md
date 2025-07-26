27.12.2024

Workflow:
1. create a repository in GitHub website
2. create a README.md file inside the vscode folder 
3. Main Step-1:initialize git: git init
4. Main Step-2: add a file for next commit: git add README.md
5. git status
6. git branch
7. Main Step-3: commit the message in staged env: git commit -m "this is my first commit"
8. git status
9. Main Step-4: make it main branch: git branch -M main
10. git branch
11. Main Step-5: git remote add origin https://github.com/polashds/GitPractice.git
12. git remote -v
13. Main Step-6: push in website: git push -u origin main

2nd session:
14. after pushing again change in README.md file: git add README.md
15. git status
16. git commit -m "second commit"
17. git push origin main: git push -u origin main

3rd session:
18. add app.py file inside the folder and add a function:
19. check: git status
20. add main.py
21. add to repository multiple files updated or new files: git add .
22. check: git status
23. change and save the README.md and add again: git add README.md
24. git commit - "third commit"
25. git push -u origin main

4th Session: 27min
gitignore:
26. create a file clicking GitHub site add file: .gitignore
27. choose.gitingore python
28. commit changes
29. to bring it to our local system: git pull origin main

5th Session: 29 min
30. create a virtual env: conda create -p venv python ==3.12 -y
31. To activate venv: conda activate  venv/

REMEMBER: WE WON'T COMMIT VENV to git repository, if we do it will upload huge GB as aresult repository will get crashed!!!!

33. check git status for the venv: git status
34. scrutinize .gitignore file: 
35. add venv/ into .gitinore after $py.class at line no 4. that means we are not going to upload venv/ folder but giving venv location direction!! : venv/

36. add a def substraction(a,b):
return a-b function at app.py file and save, then check : git status
37. to add all file : git add . 
38. git status
39. by git add . supposed to add all file and folder venv/ but this wont happened! because we have added this folder in .gitignore!!!!
40. add a myenv folder inside the venv folder, inside 100daysofcoding folder add test.py file. 
41. git status: this will show a untracked folder
42. then add myenv/ forlder in .gitihgonre after venv/ at line no 7 and save to avoid adding in the repository!!
43. git status
44. git add. 
45. git commit -m "updated gitignore"
46. git push origin main
47. cross check at git website reloading.

6th session: 
Branching Strategies: video min 36
48. to check branches in git: git branch
49. create a new git branch name-branch: git branch developera
50. to check branches in git we will see a new devlopera branch: git branch
51. create a function def division(a,b):
    return a/b at app.py and save
52. check git status: git status
53. check :git branch
54. then delete def to revert at previous stage and check: git status
55. then developera switch to branch:git checkout developera
56. then check branch: git branch
57. developera create a function def division(a,b):
    return a/b at app.py and save
58. we can see developera brach by: git status
59. developera add changes: git add .
60. we will see changes on developera branch: git status
61. developera will commit to save developera branch: git commit -m "developera story" 
62. to complete developera story, have to merge with main branch and going to switch to main bracn:git checkout main
63. after switching to main branch we wont see def division function code!
64. main developer will merge developera's code: git merge developera
65. to delete local branch: git branch -d developera
(if you dont know any command search google)
66. to check whether branch has been deleted: git status
67. to confirm : git branch
68. do not forget to push: git push origin main

7th session:
git conflict resolution: 44 min: if code updated in the website then have to pull to local
69. in the GitHub repository a developer updated code and committed def addition(a,b,c):
    return a+b+c
70. main developer worked at local git system: def substraction(a,b,c):
    return a-b-c
71. main developer do: git add .
72. main developer : git status
73. main developer : git commit -m "substraction updated"
74. main developer : git push origin main
75. problem arises, at first pull to main: git pull origin main
76. resolve conflicts!
77. then push to repository: git push origin main
78. git status
79. git add .
80. git commit -m "merge conflict"
81. to see all activity: git log 






Krish git video complete git and GitHub:
open vs code

install git cli

in terminal write git for checking

create a repository in GitHub website

download git cheetsheet

create a README.md file inside the vscode folder, here repository related info saved

Main Step-1: initialize git: git init

revealed in file explorer inside the folder by right click and revealed 

show git status untracked: git status

Main Step-2: track the ReadMe.md file changes to U to A: git add README.md

check git status: git status

clear terminal: cls

check git branch: git branch


Main Step-3: commit the message in staged env: git commit -m "this is my first commit"

Main Step-4: make it main branch: git branch -M main

check git branch: git branch

Main Step-5: git remote add origin https://github.com/polashds/GitPractice.git

Next step: git remote -v

Final Step: to push in website: git push -u origin main


first time SETUP
Configuring user information used across all local repositories
git config --global user.name “[firstname lastname]”
set a name that is identifiable for credit when review version history
git config --global user.email “[valid-email]”
set an email address that will be associated with each history marker
git config --global color.ui auto
set automatic command line coloring for Git for easy reviewing



after adding global settings have to add README.md file again: git add README.md

check : git status

commit: git commit -m "second command"

push: git push origin main

push an existing repository from the command line
git remote add origin https://github.com/polashds/GitPractice.git
git branch -M main
git push -u origin main

Example: 
add app.py file and add a function:
check: git status
add main.py
add to repository multiple files updated or new files: git add .
check: git status
change and save the README.md and add again: git add README.md



gitignore:
create a file clicking githut site add file: .gitignore

choose.gitingore python
 commit changes

to bring it to our local system: git pull origin main


.gitingore is used to file upload in repository, normally GitHub prevent large



Video min: 29min
conda create -p venv python ==3.12 -y

conda activate  venv



check git status for the venv:
git status

add venv/ into .gitinore after $py.class at line no 4.

add a def substraction(a,b):
return function at app.py file and then check git status:

git add . to add all file]

git status

add a myenv folder inside the venv folder, inside the folder add test.py file. 

then add myenv/ forlder in .gitihgonre after venv/ at line no 7

git status

git add. 

git commit -m "updated gitignore"

git push origin main

cross check at git website



Branching Strategies: video min 36

create a git branch name-branch

git branch developera



create a function at app.py

check git status

check git branch

then delete def

then check git branch

then git checkout developera

then git branch



git add .

git status

git commit -m "developera story" to save developera branch


to merge with main branch :git checkout main

git merge developera


to delete local branch: git branch -d developera

(if you dont know any command search google)



git status

git branch


git push origin main


git conflict resolution: 48 min: if code updated in the website then have to pull to local

at first pull to main: git pull origin main

then push to repository: git push origin main




to see all activity: git log 




































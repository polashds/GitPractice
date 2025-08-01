#Practicing Git commands
## git SOP
### Main Steps
1. Create a repository in github website
2. Create a local repository (folder) and open in VSCode 
3. Create README.md markdown file inside the local repository
4. Initialize git> git init
5. Add a file for next commit> git add README.md
6. Check git status> git status
7. Check git branch> git branch
8. Commit the meassage in git state> git commit -m "my meassage"
9. Make it main branch: git branch -M main
10. Add reomote git: git remote add origin https://github.com/polashds/GitPractice.git
11. Check remote git version: git remote -v
12. Push github website: git push origin main

2nd session:
13. To add many new file or change in README.md: git add .
14. git status
15. git commit -m "second commit"
16. git push origin main: git push -u origin main

gitignore:
17. create a file clicking GitHub site add file: .gitignore
18. choose.gitingore python
19. commit changes
20. to bring it to our local system: git pull origin main

Virtual Environment:
21. create a virtual env: conda create -p venv python ==3.12 -y
22. To activate venv: conda activate  venv/

#### REMEMBER: WE WON'T COMMIT VENV to git repository, if we do it will upload huge GB as aresult repository will get crashed!!!!

23. check git status for the venv: git status
24. scrutinize .gitignore file: 
25. add venv/ into .gitinore after $py.class at line no 4. that means we are not going to upload venv/ folder but giving venv location direction!! : venv/

Git Branching

# git push protection from the command line
https://docs.github.com/en/code-security/secret-scanning/working-with-secret-scanning-and-push-protection/working-with-push-protection-from-the-command-line#resolving-a-blocked-push

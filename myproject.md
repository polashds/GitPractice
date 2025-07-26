06.10.2024
git 
git config --global user.name "polashds"
git config --global user.name "polashtechai@gmail.com"
mkdir myproject
cd myproject

Note: If you already have a folder/directory you would like to use for Git:

Navigate to it in command line, or open it in your file explorer, right-click and select "Git Bash here"

Initialize Git
git init

Git Adding New Files:
So let's add some files, or create a new file using your favourite text editor. Then save or move it to the folder you just created.

For this example, I am going to use a simple HTML file like this:

Example
<!DOCTYPE html>
<html>
<head>
<title>Hello World!</title>
</head>
<body>

<h1>Hello world!</h1>
<p>This is the first file in my new Git Repo.</p>

</body>
</html>
And save it to our new folder as index.html.

Let's go back to the terminal and list the files in our current working directory:

Example
ls

Then we check the Git status and see if it is a part of our repo:

Example
git status


Git Staging Environment:
Staged files are files that are ready to be committed to the repository you are working on

For now, we are done working with index.html. So we can add it to the Staging Environment:

Example
git add index.html

The file should be Staged. Let's check the status::

Example
git status

Git Add More than One File:
A README.md file that describes the repository (recommended for all repositories):

Example
# hello-world
Hello World repository for Git tutorial
This is an example repository for the Git tutoial on https://www.w3schools.com

This repository is built step by step in the tutorial.

A basic external style sheet (bluestyle.css):

Example
body {
background-color: lightblue;
}

h1 {
color: navy;
margin-left: 20px;
}
And update index.html to include the stylesheet:

Example
<!DOCTYPE html>
<html>
<head>
<title>Hello World!</title>
<link rel="stylesheet" href="bluestyle.css">
</head>
<body>

<h1>Hello world!</h1>
<p>This is the first file in my new Git Repo.</p>

</body>
</html>

And update index.html to include the stylesheet:

Example
<!DOCTYPE html>
<html>
<head>
<title>Hello World!</title>
<link rel="stylesheet" href="bluestyle.css">
</head>
<body>

<h1>Hello world!</h1>
<p>This is the first file in my new Git Repo.</p>

</body>
</html>


Now add all files in the current directory to the Staging Environment:

Example
git add --all
Using --all instead of individual filenames will stage all changes (new, modified, and deleted) files.

Example
git status

Note: The shorthand command for git add --all is git add -A



















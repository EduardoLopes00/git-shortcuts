# git-shortcuts tutorial

<b>Platforms: windows, mac and linux</b>

This repo is a little tutorial on how to create a list of useful shortcuts to use on git.

This commands are stored inside the .gitconfig file and it can be done locally (only for the project that you're working on) or global (To all the git projects inside the machine).

Steps:

1 - Open your terminal

2 - You can set the git to open the file using the vscode. To do it, type the following command before (Optional)
  ```  
  git config --global core.editor code
  ```

3- Type the following command

  
  Local
  ```
  git config --local --edit
  ```
  
  
  Global
  ```
  git config --global --edit
  ```
  
  The .gitconfig will open either in the terminal or in the vscode (If you follow the step 2)


3 - paste the following (If there's a user section, paste above)

```

[core]
	editor = code --wait
[push]
	followTags = true
[alias]
	c = !git add --all && git commit -m
	s = !git status -s
	l = !git log --pretty=format:'%C(blue)%h%C(red)%d %C(white)%s - %C(cyan)%cn, %C(green)%cr'
	amend = !git add --all && git commit --ammend -no-edit	
  
  ```
  
  it should look like this:
  ![image](https://user-images.githubusercontent.com/60946104/194795963-ba13f055-5f41-4e54-bcfe-7a7644e78414.png)

  
  
  Explanation:
   
  - <b>c</b>: the "c" alias will concat the git add and git commit in only one command. It is highly recommended that you check your files before using it, because it will stage ALL the files that was changed.
  
  - <b>s</b>: the "s" alias will run the "git status" with the '-s' flag, which shrinks the exibition:
  ![image](https://user-images.githubusercontent.com/60946104/194796991-410df712-fba0-4aea-938e-67b85970d049.png)

  - <b>l</b>: the "l" alias will run the "git log" formatted. It is organized in a better way to vizualize the commit list:
  ![image](https://user-images.githubusercontent.com/60946104/194797166-708673f7-bfd5-44d9-b9a2-512af0af0393.png)
  
  - <b>ammend</b>: the "l" alias will take the changes, and gather it in the last commit that you've made. For example: I have commited a console.log and realized that it should be an alert instead. You run this command and it will gather the changes in the last commit, avoiding generate a new unnecessary commit

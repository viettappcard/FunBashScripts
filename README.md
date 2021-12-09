# Fun Bash Scripts
<p align="left">
	<img src="https://img.shields.io/badge/platform-ubuntu-blueviolet?style=for-the-badge"
			 alt="platform">
	<img src="https://img.shields.io/badge/language-bash-blue?style=for-the-badge"
			 alt="language">
</p>

## General Information
Bash scripts to increase work flow. For personal use but welcome all to use and add to.

I make symlinks for them within /usr/local/bin .

## Scripts

1. AddCommitPush

Takes in argument and add all files, commit with argument as message and push to origin master

2. CommitPush

Take in argument, commit with argument and push to origin master

## Command line
1. Find files larger than 50MB in current directory and children:
   ```bash
   $ find . -type f -size +50M
   ```
   current dir only:
   ```bash
   $ find . -maxdepth 1 -type f -size +100M
   ```

2. Find processes that are Listening on ports:
   ```bash
   $ sudo lsof -i -n -P | grep LISTEN
   ```
## git commands

1. Keep either files in merge conflicts. Taken from <a href="http://gitready.com/advanced/2009/02/25/keep-either-file-in-merge-conflicts.html">Link</a>
   ```bash
   $ git checkout --ours keep_local_current_branch_file
   $ git checkout --theirs keep_other_branch_file
   ```
2. Push to single branch. If your Local branch and remote branch is the same name then you can just do it:
   ```bash
   $ git push origin branchName
   ```
   When your local and remote branch name is different then you need to do the following:
   ```bash
   $ git push origin localBranchName:remoteBranchName
   ```

3. If you're in the business of merging unrelated histories
   ```bash
   $ git pull --allow-unrelated-histories
   ```

4. To push to remote branch that does not have same name as local branch:
   ```bash
   $ git push remote local_branch:remote_branch
   ```
   
5. To checkout a remote branch and work on it
   ```bash
   $ git checkout --track origin/newsletter
   ```
   
6. To revert commit without losing changes. Taken from <a href="https://stackoverflow.com/questions/19859486/how-to-un-commit-last-un-pushed-git-commit-without-losing-the-changes">a nice StackOverflow exchange</a>
   ```bash
   $ git reset HEAD~1 --soft  
   ```

## Author and Acknowledgements
Author: Viet Than, thanhoangviet@gmail.com<br>

## git config
```bash
git config --list
git config --global --list

git config --global user.name '<USER>'
git config --global user.email '<EMAIL>'
git config --global pull.rebase true
```

## git local
```bash
git init					# create new repo

git add <FILE>					# place file in staging environment
git add -A					# place all files in staging environment

git commit -m "<DESCRIPTION>"			# commit to repo
git log						# history of commits

git status                      		# state files in repo

git branch					# list all branches
git branch <NEW_BRANCH>				# create new branch
git branch -d <BRANCH>				# delete branch
git checkout <BRANCH>				# move to branch
git checkout -b <BRANCH>			# create new branch, and move to branch

'pull' is a combination of:
- fetch
- merge/rebase

git submodule add <URL>				# add submodule

git submodule deinit -f <DIRECTORY>/<REP>	# remove submodule - part 1
git rm -f <DIRECTORY>/<REP>			# remove submodule - part 2
rm -rf .git/modules/<DIRECTORY>/<REP>		# remove submodule - part 3

git clone --recurse-submodules <REPO>
	git clone <REPO>			# clone repo
	git submodule update --init
		git submodule init		# initialize (checkout) local configuration file
		git submodule update		# fetch all data from submodule
git pull --recurse-submodules
```

## github remote
```bash
git remote set-url origin git@github.com:<USER>/<REP>.git

git remote add origin <URL>			# add remote repo, with specified URL as origin, to local repo
git push -u origin main				# push main branch to origin URL, and set as default remote branch
```

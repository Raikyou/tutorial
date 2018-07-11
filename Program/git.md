### Configuration

```ruby
git config --global user.name "Your Name"
git config --global user.email "email@example.com"

ssh-keygen -t rsa -C "your_email@example.com"
```

### Create Repository

```bash
git init [project-name]    % creates a new local repository with the specific name
git clone [url]            % downloads a project and its entire version history
git add <file>
git add .        % modified and new file
git add -u        % modified and deleted
git add -A        % all
git commit -m "add a new file"
git remote add origin git@github.com:user/project.git
git push -u origin master
git clone git@github.com:user/project.git
```

### Making Changes

```
git status        % lists all new or modified files to be commited
git diff            % shows file differences not yet staged
git add [file]    % snapshots the file in preparation for versioning
git diff --staged   % shows file differences between staging and the last file version
git reset [file]    % unstages the file, but preserve its contents
git commit -m "[message]"   % records file snapshots permanently in version history
```

### Group Changes

```
git branch            % lists all local branches in the current repository
git branch [branch-name] % creates a new branch
git checkout [branch-name] % switches to the specified branch and updates the working directory
git checkout -b [branch-name] % creates and switches to a new branch
git merge --no-ff [branch]     % combines the specified branch's history into  the current branch
git branch -d [branch-name]    % deletes the specified branch
```

### Refactor Filenames

```
git rm [file]        % deletes the file from the working directory and stages the deletion
git rm --cached [file]    % removes the file from version control but preserves the file locally
git mv [file-original] [file-renamed]   % changes the file name and prepares it for commit
```

### Suppress Tracking

```
*.log          % a text file named .gitignore suppress accidental versioning of files and paths matching specified patterns
build/
temp-*       
git ls-files --other --ignored --exclude-standard  % lists all ignored files in this project
```

### Save Fragments

```
git stash    % temporarily stores all modified tracked files
git stash pop    % restores the most recently stashed files
git stash list    % lists all stashed changesets
git stash drop     % discards the most recently stashed changeset
```

### Review History

```
git log    % lists version history for the current branch
git log --follow [file]        % lists version history for a file, including renames
git diff [first-branch] ... [second-branch]    % shows content differences between two branches
git show [commit]        % outputs metadata and content changes of the specified commit
```

### Redo Commits

```
git reset [commit]    % undoes commits after commit, preserving changes locally
git reset --hard [commit]    % discards all history and changes back to the specified commit
git reset --hard HEAD^          % back to the last version
git reset --hard HEAD^^          % back to the last two version
git reset --hard HEAD~100        % back to the last 100 version
git reset --hard commit_id
```

### Synchronize Changes

```
git fetch [bookmark]    % downloads all history from repository bookmark
git merge [bookmark]/[branch]    % combines bookmark's branch into current local branch
git push [alias][branch]    % uploads all local branch commits to Github
git pull    % downloads bookmark history and incorporates changes
```

```

```

### Other Command

```
git log --pretty=online --graph        % show commit history
git reflog                        % show command log
```




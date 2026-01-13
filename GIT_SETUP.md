pwd (print working directory – shows the exact path of the current directory)

cd (change directory – move to another directory)
cd ~ (go to the user home directory)
cd ~/projects (go to the projects directory)
cd ~/projects/linux-git-basics (enter the repository directory)

ls (list – shows files and directories)
ls -la (list all – detailed view including hidden files)

mkdir projects (creates the projects directory)
mkdir -p ~/.ssh (creates the .ssh directory, -p also creates parent directories if missing)

chmod 700 .ssh (changes permissions: 7=rwx owner, 0=--- others; only the user has access)

echo ~ (prints the home directory path)
echo $SSH_AGENT_PID (prints the PID of the ssh-agent process)

git init (initializes a git repository – creates the .git directory)
git status (shows repository status: modified, staged, untracked files)
git add README.md (adds a file to staging)
git add . (adds all changes to staging)
git commit -m "message" (creates a snapshot of changes with a commit message)

git log (shows commit history)
git log --oneline (compact commit history view)

git branch (shows branches and the currently active branch)
git branch -M main (renames the current branch to main, -M = force rename)

git config --global user.name "Name" (sets the commit author name globally)
git config --global user.email "email" (sets the commit author email globally)
git config --global --list (shows global git configuration)

git remote -v (shows remote repositories with fetch/push URLs)
git remote add origin git@github.com
:USER/repo.git (adds GitHub repository as origin)
git remote get-url origin (shows the exact origin URL)

git push -u origin main (pushes commits to GitHub; -u links local and remote branches)
git push (pushes changes once upstream is set)
git pull (pulls the latest changes from GitHub)

ssh-keygen -t ed25519 -C "email" (generates an SSH key; ed25519 = algorithm, -C comment)

ls -la ~/.ssh (lists the contents of the .ssh directory)
cat ~/.ssh/id_ed25519.pub (prints the public key – this is the one added to GitHub)

eval "$(ssh-agent -s)" (starts ssh-agent and sets environment variables in the shell)
ssh-add ~/.ssh/id_ed25519 (adds the private key to ssh-agent)
ssh-add -l (lists keys currently loaded in ssh-agent memory)

ssh -T git@github.com
 (tests SSH authentication to GitHub, -T disables shell access)

echo "text" > README.md (writes text to a file – overwrite)
echo "text" >> README.md (appends text to the end of a file)pwd (print working directory – shows the exact path of the current directory)



## Git Commands

### Checking Status

- **Check git status**
  ```sh
  git status
  ```
  **Example:**
  After modifying a file (`index.js`), run `git status` to check its state before adding it to staging.

### Adding Files to Staging Area

- **Add one file to staging area**
  ```sh
  git add <filename>
  ```
  **Example:**
  ```sh
  git add index.js
  ```
  This adds `index.js` to the staging area.

- **Add all files to staging area**
  ```sh
  git add -A
  git add --a
  git add .
  ```
  **Example:**
  ```sh
  git add .
  ```
  This adds all modified and new files in the repository to staging.

### Committing Changes

- **Perform a Git commit**
  ```sh
  git commit -m "Commit message"
  ```
  **Example:**
  ```sh
  git commit -m "Added new feature to homepage"
  ```

- **Direct commit without staging**
  ```sh
  git commit -a -m "Commit message"
  ```
  **Example:**
  ```sh
  git commit -a -m "Updated styles in CSS files"
  ```

### Checking and Comparing Changes

- **Checkout one file**
  ```sh
  git checkout <filename>
  ```
  **Example:**
  ```sh
  git checkout index.js
  ```
  Restores `index.js` to the last committed state.

- **Checkout all files from the last commit**
  ```sh
  git checkout -f
  ```

- **Check recent activities (last 2 commits with changes)**
  ```sh
  git log -p -2
  ```

- **Compare working tree to staging area**
  ```sh
  git diff
  ```

- **Compare last commit to staging area**
  ```sh
  git diff --staged
  ```

### Removing Files

- **Delete from staging area to untracked**
  ```sh
  git rm --cached <filename>
  ```
  **Example:**
  ```sh
  git rm --cached config.json
  ```
  This removes `config.json` from version control but keeps it locally.

- **Delete file completely**
  ```sh
  git rm <filename>
  ```
  **Example:**
  ```sh
  git rm old_script.js
  ```

- **Remove `node_modules` from Git and ignore it in future commits**
  ```sh
  git rm -r --cached node_modules
  echo "node_modules/" >> .gitignore
  git add .gitignore
  git commit -m "Removed node_modules and updated .gitignore"
  git push origin main
  ```
  **Example:**
  If you accidentally committed `node_modules`, this removes it and prevents future commits.

### Short Status View

- **Show short status**
  ```sh
  git status -s
  ```
  **Example:**
  Displays a compact version of `git status`, showing modified (`M`), new (`A`), and deleted (`D`) files.





### Remote Repository Setup

- **Set remote repository**
  ```sh
  git remote set-url origin git@github.com:iam-rajuan/WebDevelopmentProjects.git
  ```
  **Example:**
  If you change your GitHub repository URL, use this command to update it.

- **View remote repositories**
  ```sh
  git remote -v
  ```

### Pushing Changes to GitHub

- **Push to master branch**
  ```sh
  git push origin master
  ```
  **Example:**
  ```sh
  git push origin main
  ```
  Pushes changes to the `main` branch.

- **Push to a specific branch**
  ```sh
  git push origin branch1
  ```

- **Set upstream and push**
  ```sh
  git push -u origin master
  ```

- **Push using the set upstream**
  ```sh
  git push
  ```

## Ignoring `package-lock.json` and `node_modules` in Git  

### 1. Modify `.gitignore` in Your Repository  
To ignore `package-lock.json` and `node_modules/` from all folders inside a specific repository, add the following lines to the `.gitignore` file at the root of your project:  

```gitignore
**/package-lock.json
**/node_modules/
```  

This ensures that `package-lock.json` and all `node_modules/` folders are ignored throughout the repository.  

### 2. Use a Global `.gitignore` (For All Repositories)  
To ignore `package-lock.json` and `node_modules/` in all your Git repositories, follow these steps:  

```sh
git config --global core.excludesfile ~/.gitignore_global
```  

Then, edit `~/.gitignore_global` and add:  

```gitignore
**/package-lock.json
**/node_modules/
```  

### 3. Remove Already Tracked `package-lock.json` and `node_modules/` Files  
If `package-lock.json` and `node_modules/` have already been committed, remove them from tracking:  

```sh
git rm --cached **/package-lock.json
git rm -r --cached **/node_modules/
git commit -m "Removed package-lock.json and node_modules from tracking"
git push origin main  # or your current branch
```  


  
















### SSH Key Setup

- **Generate SSH key**
  ```sh
  ssh-keygen -t rsa -b 4096 -C "rajuan.official@.com"
  ```

- **Start SSH agent**
  ```sh
  eval $(ssh-agent -s)
  ```

- **Add SSH key to agent**
  ```sh
  ssh-add ~/.ssh/id_rsa
  ```

- **View SSH public key**
  ```sh
  cat ~/.ssh/id_rsa.pub
  ```


# VS Code Shortcuts

# Terminal Command

- **Go back to user location**
```sh
cd
```
- **Go back Previous location like backward**
```sh
cd -
```
- **Change C: to D:**
```sh
D: 
```
- **Previous Directory**
```sh
cd ..
```
- **Close Terminal and Open Existing Directory**
```sh
code -r <dirname> 
code -r ExpressJS 
```

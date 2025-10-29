# mirroring Repository (from GitLab to GitHub)
 


## Overview / Architecture :

![](/img/Architecture.png)

Repository mirroring is the process of keeping one repository(the mirror) automatically synchronized with another(the source). This means that whenever new commits, tags are pushed to the source repository, they are replicated to the mirror.

## This is Useful for :
 -  Backup : Provides an automated versioned backup of your repository history.
 -  Faster Access for Distributed Teams : Developers across different regions can clone or pull from local mirror.

 - Multi-Environment Synchronization : Keep development, staging, and production repos aligned (e.g. mirror the main repo into a staging repo for test) 

 ## Step-1 : Create Repository in GitHub
 Create  a repository with README.md file :

 ![](/img/GitHub_Repo.png)

  ## Step-2. Create Personal Access Token(classic)

- GitHub -- Settings -- Developer setting -- Personal Tokens -- Generate New token
- Grant all permissions

![](/img/Token_Creation.png)

## Copy the token :

![](/img/Classis-Token.png)

## Psate the token :

![](/img/Paste-Token.png)

## Step-3. Create a Repository in GitLab
Create a Blank repository with readme.md file :

![](/img/GitLab_Repo.png)

## Step-4. Create a mirroring Repository
Set up your project to automatically push or pull changes to another repository. Branches, tags, and commits will be synced automatically.

- Open your project -- Setting -- Repository -- Mirroring repository.

- Click on "mirror repository".

- for the Git Repository URL use the HTTPS push URL in this form:
 
         https://<GITHUB_USERNAME>@github.com/<GITHUB_USERNAME>/<GITHUB_REPO>.git

- When prompted for a password, paste the GitHub access token and save it.

![](/img/itHub_Repo_URL.png)

## Step-5. Clone GitLab repository in your machine, and files and push it to the server

![](/img/Git-Clone-FileAdd-Push-Process.png)

## Output 

### In GitLab :

![](/img/Mirror-Add-File-GitLab.png)

## In GitHub

Automatically index.html file is synchronized to GitHub repository.

![](/img/Mirror_add-File-GitHub.png)

# Conclusion

Mirroring keeps your GitLab and GitHub repos in sync automatically.
It ensure bakups, accessibility, and collaboration across platforms.
Using GitLab's push mirror makes syncing automated, secure, and efficient, so your code is always up to date
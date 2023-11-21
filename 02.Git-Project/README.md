# Git Project

## Basic Git Project Implementation

### 01. Initializing a Git Repository

#### - Here, we create a working folder or directory

#### - Move into our working folder

#### - Then run command *`git` `init`*

See illustration below: 

![git_init_comman](./img/01.git_init.png)


### 02. Git commit

#### - To do this, in our working directory we created a file *`touch` `index.txt`*

#### - Wrote a sentence in that file, saved our changes,

#### - Added our change to git staging using command *`git` `add`*

#### - We then committed to git using command *`git` `commit`* *`-m` `"Project 2-Git"`*

See illustration below: 

![git_commit](./img/02.git_Commit.png)


## Working with Branches

In Git, a branch is a new/separate version of the main repository. 

### 03. Making a new Branch

#### - We use *`git` `checkout`* *`-b`* in creating a new branch

#### - The *`-b`* helps us create or change into the new branch

See illustration below: 

![git_checkout](./img/03.git_checkout.png)



### 04. Listing Git Branches 

We use this command to list branches.

#### - This can be achieved with command *`git` `branch`*

See illustration below: 

![git_branch](./img/04.git_branch.png)


### 05. Changing into an Old Branch

#### - To change into an existing branch,

#### - We use the command *`git` `checkout`* *`<branch-name>`*

See illustration below: 

![git_checkout_branchname](./img/05.git_checkout_branchname.png)

### 06. Merging a Branch to Another Branch

To merge branches locally, use git checkout to switch to the branch you want to merge into. This branch is typically the main branch. Next, use git merge and specify the name of the other branch to bring into this branch

#### - First we change into our main branch

#### - Then run git command *`git` `merge`* *`<branch-name>`*

See illustration below: 

![git_merge](./img/06.git_merge.png)


### 07. Deleting a Git Branch

#### - The command to delete a local git branch can take one of the following two forms: *`git`* *`branch`* *`--delete`* *`<old-branch>`*, *`git`* *`branch`* *`-d`* *`<old-branch>`*

See illustration below:

![git_branch_delete](./img/07.git_branch_delete.png)




## Collaboration and Remote Repository


### 08. Create a New Reporository

#### - Here, first we created a github account at *`(https://github.com/join)`*

#### - After completion of account creation we created a new repository

See below:

![git_repository_creation](./img/08.create_new_repository.png)


### 09. Git add origin

#### - Copying the code from the newly created repository, we pasted on `git` `bash`

See illustration below:

![git_origin](./img/09.adding_remote_repo.png)


### 10. Push origin

#### - After committing changes to local repo, we pushed content to remote repo.

See illustration below:

![git_push](./img/10.push_remote_repo.png)


### 11. Cloning Remote Git Repository

See illustration below:

![git_clone](./img/11.clone_repo.png)




## Branch Management and Tagging


### Introduction to Markdown Syntax


### 12. Headings

To create headings, we use the hash(#) button symbol at the beginning of the line. 

#### - The number of hash(#) symbol used indicates the level of the heading

See example below:


![headings](./img/12.markdown_syntax_headings.png)



### 13. Emphasis

#### - Asterisks or Underscore is used here 

See example below:

![emphasis](./img/13.markdown_syntax_emphasis.png)


### 14. Lists

#### - Markdown has support for both ordered and unordered type of list

See examples below:

![lists](./img/14.markdown_syntax_list_examples.png)



### 15. Links

#### - To create hyperlink, use square-brackets "[]" for the link, followed by parentheses containing the URL.

See examples below:

![link](./img/15.markdown_syntax_link.png)


### 16. Images

#### -  To display images, we use an exclamation mark "!", followed by square-brackets "[]" for the alt text and parentheses containing the URL.

See example below:

![images](./img/16.markdown_syntax_images_examples.png)


### 17. Code

#### - To display code or code snippets, use backticks (`) to enclose the code.

See example below:

![code](./img/17.markdown_syntax_code_display.png)
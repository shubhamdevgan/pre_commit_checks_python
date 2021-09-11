# pre_commit_checks_python
This Repo contains some of the standard Pre-Commit checks or Pre-commit hooks, with standard settings for checks to be performed.
With pre-commit hooks you can focus on writing the actual code and logical parts of your code, rather than to worry about the coding standard and once you are done with code ,the pre-commit checks will help you to format and style code in compliance to PEP8 rules, making code structure in line with standard practices and helping others understand and use it easily.

Pre-commit checks are checks perfomed automatically when you make a commit, once a commit command is fired the pre-commit hooks will check the staged files for 
the their compliance with PEP8 standard and black code style, Once the check is run the pre-commmit hooks will modify the files according to PEP8 rules and the modified file will be added to  unstaged area, where you can check the changes made by hooks and verify them and then again add and commit them, only commits which pass all the checks will be actually commited to git ,commits which don't pass checks will not be commited.

![pre-commit_flow](https://user-images.githubusercontent.com/28834720/132936889-b12582e3-02dd-49b6-81cd-a50fc5b18c7c.png)

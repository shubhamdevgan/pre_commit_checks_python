# pre_commit_checks_python
![https://github.com/ambv/black](https://img.shields.io/badge/code%20style-black-000000.svg)

This Repo contains some of the standard Pre-Commit checks or Pre-commit hooks, with standard settings for checks to be performed.
With pre-commit hooks you can focus on writing the actual code and logical parts of your code, rather than to worry about the coding standard and once you are done with code ,the pre-commit checks will help you to format and style code in compliance to PEP8 rules, making code structure in line with standard practices and helping others understand and use it easily.

Pre-commit checks are checks perfomed automatically when you make a commit, once a commit command is fired the pre-commit hooks will check the staged files for 
the their compliance with PEP8 standard and black code style, Once the check is run the pre-commmit hooks will modify the files according to PEP8 rules and the modified file will be added to  unstaged area, where you can check the changes made by hooks and verify them and then again add and commit them, only commits which pass all the checks will be actually commited to git ,commits which don't pass checks will not be commited.

![pre-commit_flow](https://user-images.githubusercontent.com/28834720/132936889-b12582e3-02dd-49b6-81cd-a50fc5b18c7c.png)


Install Required packages:

```
pip install pre-commit
pip install black
pip install flake8
pip install isort
pip install interrogate
```

Steps to setup:
1. Install the required packages
2. Download the config files and place them into root directory of project
3. add `.` in pre-fix of the config file names by renaming them, ex: rename `flake8` to `.flake8` , except for `pyproject.toml` the `pyproject.toml` file will not be renamed.
4. run `pre-commit install` to install precommit file to git config automatically, you should see output `pre-commit installed at .git/hooks/pre-commit` .
5. all done, now just commit you code , the pre-commit checks will run automatically to check your code and return results.

Incase your config files don't work,try by moving the `.flake8` and `pyproject.toml` files to directory in which `.git` is stored.

**IMP:** To skip a particular commit from pre-checks , add `--no-verify` to commit,
         example: `git commit -m 'commit to skip example' --no-verify`

**Notes:**

files that contain this line are skipped: `# flake8: noqa`

lines that contain a `# noqa` comment at the end will not issue warnings.

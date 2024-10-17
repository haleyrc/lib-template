# lib-template

Foundational elements for creating new "library" packages.

---

## Usage

> **N.B.:** The commands in this section assume you have set the `REPO_NAME` variable e.g.:
> ```sh
> REPO_NAME=mypkg
> ```

To make use of this template, you will need to create a new repository and pass this repository as the template argument.
To do this with the GitHub CLI you can run something like:

```sh
gh repo create $REPO_NAME --template https://github.com/haleyrc/lib-template --public
```

You can now pull down the repository to your local machine using:

```sh
git clone git@github.com:haleyrc/$REPO_NAME.git
```

Now you'll want to do some housekeeping so run:

```sh
cd $REPO_NAME
```

followed by:

```sh
go mod init github.com/haleyrc/$REPO_NAME
```

Next, you'll want to modify the repository README to match your package name, description, etc.
Note that you should be modifying the `README.md` file at the _root_ of the repository and not _this_ file.
Once that's done, you can delete this file which will make the repository README the default.

Finally, you can add everything to Git and amend the default initial commit created by the template:

```sh
git add .
git commit --amend -m "chore: Initial commit"
git push -f
```

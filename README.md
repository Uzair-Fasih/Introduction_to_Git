## Git Tutorial: Handling Merges and Pull Requests

### Prerequisites:

- Basic knowledge of Git commands.
- A GitHub account.

### Objective:

By the end of this tutorial, you should be able to:

1. Clone a repository.
2. Make changes and push them.
3. Raise a pull request (PR).
4. Resolve merge conflicts.

### Let's Get Started!

#### 1. Fork the Repository:

Start by forking the existing repository. This repository is located on a remote server, which is typically GitHub for most projects. By forking it, you create a local copy which you can edit and push back to the remote repository.

> When you fork the project, make sure to unselect the option to Copy the main branch only

Next clone the repo

```bash
$ git clone https://github.com/[YOUR_GITHUB_ID]/Introduction_to_Git/
```

If you check the repo, you should see the two branches `main` and `dev`

```bash
$ git branch -a
```

#### 2. Create a New Branch:

Checkout out the remote `dev` branch and then create a new branch from dev using the following command

```bash
$ git checkout remotes/origin/dev
$ git checkout -b [your_name]-choice
```

Replace `[your_name]` with your actual name.

#### 3. Choose Your Greek God:

Open the provided text file `greek_gods.tx` in the repository. Choose one Greek god from the following list and __replace__ the one in the file:

- Hera
- Poseidon
- Demeter
- Athena
- Apollo
- Artemis
- Ares
- Aphrodite
- Hephaestus
- Hermes
- Dionysus

Save and close the file.

#### 4. Commit and Push:

Commit your changes and push them to your branch on the remote GitHub repository.

```bash
$ git add .
$ git commit -m "Chose my Greek god"
$ git push origin [your_name]-choice
```

#### 5. Raise a Pull Request:

Now, return to the GitHub repository online:

1. Click on "Pull Requests".
2. Select "New Pull Request".
3. For the base branch, choose "main" **from your Fork**. For the compare branch, pick your branch (`[your_name]-choice`) **from your Fork**.
4. Review your changes and click "Create Pull Request".
5. Add a title and description for your PR and submit.

If you encounter conflicts during the PR (which is expected given the Greek god choice), proceed to step 6.

#### 6. Resolve Merge Conflicts:

Open the text file on GitHub by selecting the option to `Resolve Conflicts`, and on the web editor you'll see conflict markers:

```
<<<<<<< HEAD
Apollo
=======
Athena
>>>>>>> [commit_hash]
```

To resolve this:

1. Decide which choice to keep or combine them (in this case, keep your changes).
2. Remove the conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`).
3. Save the file.

After resolving all conflicts, create the PR

#### 6. Merge the PR

Finally, merge the PR.

Congratulations! You've now tackled changes, navigated conflicts, and initiated a PR. Handling merge conflicts can seem daunting at first, but with practice, it becomes intuitive. This exercise imparts the collaborative flow of team projects using Git and
GitHub, enhancing your version control skills.

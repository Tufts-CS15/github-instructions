# Welcome to Github :elephant:
## Creating an account

You can create a personal Github account following the [directions here](https://docs.github.com/en/get-started/start-your-journey/creating-an-account-on-github#signing-up-for-a-new-personal-account). 

> [!NOTE]
> It is reccomended that you use a personal email address, not your Tufts email address as your accounts primary email so that you can use your Github account after graduatation. You can then add your Tufts email [as an additional email](https://docs.github.com/en/account-and-profile/how-tos/email-preferences/adding-an-email-address-to-your-github-account) if desired.

### Accessing your account on Halligan

It is reccomended that you setup an ssh key to easily authenticate on the halligan server.
You can do this by following the instructions [here](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#generating-a-new-ssh-key) for `Generating a new SSH key` and `Adding your SSH key to the ssh-agent`, then adding the SSH key to your Github account using [these instructions](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account#adding-a-new-ssh-key-to-your-account).

### TODO Update SFTP?
Should `.git` files are excluded from SFTP? Do we want to only talk about Halligan, or mention that students can clone on their local machines and then sync to Halligan as an alternative.

## Starting an assignment

Links for accessing each assignment will be posted on Piazza. However, you can practice with the CS15 Starter Project which you can find [at this link](https://classroom.github.com/a/rFkH85E7).

Selecting that link will allow you to create a new assignment. You will then get an invitation (accessible through your email or Github) to collaborate with CS15:

<img width="678" height="723" alt="image" src="https://github.com/user-attachments/assets/750af04e-672a-4ccd-9f72-5174b489a4e1" />

After you accept the invite, you can navigate to the project and clone it you your halligan account by copying the clone ssh command:

<img width="676" height="410" alt="image" src="https://github.com/user-attachments/assets/a88ff313-0d69-4171-bf35-1ebdce66cc78" />

You can then clone the assignment to your halligan account and setup your project. For instance, for metrosim you would run the command (replacing `csmagnano` with your Github username:

```
git clone git@github.com:Tufts-CS15/metrosim-csmagnano.git
```

You then would `cd` into the created directory created cloning the repo:

```
cd metrosim-csmagnano
```

And setup metrosim using the `/comp/15/files/metrosim/setup` script.

> [!NOTE]
> Typically, project repositories will only contain a `.gitignore` file and a starter `README`. You need to add the rest of the files as per the spec instructions! 

Once your project is setup, you'll want to make an initial `commit`:

```
git add . # Adds all files in current directory
git commit -m "Initial commit" # Make a commit with all initial file states
git push origin main # Push to the remote repository on Github. 
```

Note that you only need to specify `origin main` on your first push.

## Using git during your assignment

You're now all set to go! Add your changes and new files, make commits, and push! You now have an easy way to check your progress, save your work, redo and undo changes, etc. If you are working from multiple locations (this will matter much more for the group project `gerp`) you should make sure to run `git pull` before you start editing files each time. 

> [!WARNING]
> A common mistake is to forget to add files with `git add`. You need to `add` any new files or files that you have edited before making a commit. It is a good idea to get into the habit of running `git status` to check which local changes are staged before commiting. 

We reccomend you consider making a commit whenever:
* You complete a significant chunk of work (finish a file or bigger method, get some functionality working or squash a bug, etc.).
* Reach a code state you might want to return to (you debate whether to change a function to be recursive, and might want to undo that decicion later if it doesn't work out).
* Finish your coding session. 

## Adding to your readme

If you decide to use git, you will recieve 2 bonus points on your assignment. In order to recieve the bonus points, you **must**:
* Have at least 5 significant commits (i.e. don't just commit 1-line changes 5 times right before you handin your files).
* In your README header add the line `Github Repository: link-to-repo`, as in for instance `Github Repository: https://github.com/Tufts-CS15/starter-assignment-csmagnano`.  

> [!IMPORTANT]
> You need to make mention of your repository in your README! If you do not, you will NOT recieve credit. 

## Turning in to Gradescope

When turning your project into Gradescope, you can now use the Github option:

<img width="413" height="343" alt="image" src="https://github.com/user-attachments/assets/c6a50b1b-783f-436d-9574-cba51e714b0f" />

The first time you submit to Gradescope via github, you will need to authorize your Github account. You may also need to go into your Github account settings under `Settings -> Integrations -> Applications` and request/grant acccess for `Tufts-CS15`:

<img width="575" height="232" alt="image" src="https://github.com/user-attachments/assets/2e145f5c-7be9-4b74-8619-2c66bef095c2" />

You can then select the repository and branch (most likely `main`) that you want to submit. 

> [!IMPORTANT]
> Make sure you push your changes before submitting!

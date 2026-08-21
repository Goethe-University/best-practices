<img width="1618" height="121" alt="grafik" src="https://github.com/user-attachments/assets/c92ae18c-ec9d-479d-9bb1-850bd427cbd0" />

---

For collaborative work on a project, a local RStudio project can be connected to a GitHub repository. This allows changes to be versioned, shared, and synchronized among all project members.

For further information and possible applications, see also https://happygitwithr.com/

---

### 1. Open the project in RStudio to enable Git:

Tools > Version Control > Project Setup: Select Git under Version control system and confirm by clicking OK.

<img width="751" height="406" alt="grafik" src="https://github.com/user-attachments/assets/e5b10c91-bdec-4016-ae12-7f2f09bb0f1a" />

<img width="769" height="686" alt="grafik" src="https://github.com/user-attachments/assets/0c0f3d20-40a2-4ecb-8a64-fa49f94ec908" /> 

At this point, RStudio will ask whether a repository should be created automatically. Confirm by selecting ‘Yes’

<img width="798" height="728" alt="grafik" src="https://github.com/user-attachments/assets/2caab214-dee2-4f4e-8d90-ee7591049dc6" />

**PLEASE NOTE: RStudio must be restarted at this point (you will also be prompted to restart it immediately). After restarting, a new “Git” tab will appear in the upper-right pane.**

---

### 2. The first commit

Before the project can be synchronized with GitHub, an initial version of the project must be created in Git (the first commit).

Open the Git tab and click “Commit”. A new window will open.

<img width="797" height="365" alt="grafik" src="https://github.com/user-attachments/assets/ba4a852a-4e3a-41c3-8ce6-879d657bc64d" />

 Enter a meaningful description of the project's current state here. For the first commit, something like “Initial project setup” is often used. Then confirm by clicking the “Commit” button.

 <img width="830" height="316" alt="grafik" src="https://github.com/user-attachments/assets/cfb0adb6-91fb-4240-80f3-1d089766dee5" />

**NOTE: Changes must be saved in the files before they can be committed!**

---

### 3. Go to GitHub and create an empty repository:

In your GitHub account, go to “Repositories” and click the “New” button in the top right-hand corner. Create an empty repository by entering a Repository name and clicking “Create repository”.

Do not add a .gitignore file or a README.

 <img width="783" height="766" alt="grafik" src="https://github.com/user-attachments/assets/2de2f942-d679-4924-b039-70656da6e0c7" />

**NOTE: Repositories are public by default. The visibility can be changed at any time in the repository settings.**

Copy the repository’s HTTPS URL.

<img width="807" height="274" alt="grafik" src="https://github.com/user-attachments/assets/ac8464a8-1e65-430e-8c49-3721f38b1ed9" />

 ---

 4. Open a new terminal in RStudio

Check the path; it should be the project folder.


 <img width="939" height="524" alt="grafik" src="https://github.com/user-attachments/assets/7dbd5c3c-1d73-44f2-9b76-17d4ca752e4d" />

```
git remote add origin <https-Adresse>

```

Enter the address without the < > brackets.

You can use ```git remote -v``` to check whether the connection has been set up correctly. The output should look like this:

```
origin https://github.com/... (fetch)
origin https://github.com/... (push)
```

Next, push the changes to GitHub: 

```git push -u origin main```

If GitHub asks for your login details at this point, enter them.

The local Git repository is now connected to GitHub. Changes can now be committed via RStudio or using Git commands in the terminal, and synchronised with GitHub.

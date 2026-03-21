# git_assignment_HeroVired
# git_assignment_HeroVired

**Q1 Assignment Steps:** 

**1:creted new branch "dev" and scitch**

      git checkout -b dev

      **addded code "feature: calculating the square root of a number to CalculatorPlus.py file**

**Executed Git commands:**

      git add CalculatorPlus.py

      git commit --m :Implemented feature: calculating the square root of a number:

      git push origin dev

2:merged dev to main branch: switched to main branc and executed this  commands: 

   **Executed Git command**

      git merge  --no-coomit --no-ff dev

      git commit --m "comment"

      git pusg origin main

      Command Breakdown: 

        --no-ff(No Fast-Forward): This forces Git to create a merge commit even if it could have performed a "fast-forward"

        --no-commit: This tells Git to perform the merge but stop just before creating the final merge commit.

                      This allows you to inspect the merged files and make  manual adjustments before the changes are officially recorded.

  **3: Pushed code to main branch**

        **Executed Git command**

         git push origin main

**4: To release of version 1 need to create relase tag;**

        **Executed Git commands:**

         git tag -a v1.0.0 -m "Release version 1 of Calculator Plus App"

            **Git Command Breakdown:**

            git tag:** The base command to create a "bookmark" in your history.

            -a (Annotated):** Creates a full object in the Git database. It includes the tagger name, email, date, and a message. This is the standard for       releases.

            v1.0.0: The name of your tag. Following Semantic Versioning (Major.Minor.Patch) is best practice.

            -m "...": The description of what this version includes.

**5:Push created release tag to git gub main branch;**

     **Executed Git commands:**

     git command: git push origin v1.0.0

**6:Implemented feature/sqrt:**

     **Executed Git commands:**

       git checkout -b feature/sqrt

       added bug fixation code 

       Push code Feature bracn

     **Executed Git commands:**

         git push origin feature/sqrt

**7: Cteated Pull Request from feature/sqrt to Dev branch.**

**8: Finally Tested on dev branch and merged it to Main Brach.**

**9:To release of version 1 need to create relase tag;****

   **Executed Git commands:**

      git tag -a v2.0.0 -m "Release version 1 of Calculator Plus App"

      **Git Command Breakdown:**

      git tag:** The base command to create a "bookmark" in your history.

      -a (Annotated):** Creates a full object in the Git database. It includes the tagger name, email, date, and a message. This is the standard for       releases.

            v2.0.0: The name of your tag. Following Semantic Versioning (Major.Minor.Patch) is best practice.

            -m "...": The description of what this version includes.
 
**===================================================================================================================================================================**

**Q2 Assignment Steps:**
 
1. Created a new branch

   **Executed Git Commands**:

      git branch lfs

      **This creates a new branch named lfs. It’s good practice to test LFS setup on a separate branch before merging it into your main project.**

2. Initialized Git LFS

   **Executed Git Commands:**

      git lfs install   

      **This sets up Git LFS on your local machine. You only need to do this once per user account to ensure Git knows how to handle LFS pointers.**

3. Generated a dummy large file:

   **Executed Git Commands**:

      fsutil file createnew Sample01.bin 209715200

      fsutil file createnew Sample01.iso 209715200

   **This is a Windows command that creates a blank file named Sample01.bin. The number 209715200 makes it exactly 200 MB, which is the perfect size to test LFS.**

5. Tell LFS which files to track:

   **Executed Git Commands**:

      git lfs track "*.bin"

      **This instructs Git LFS to take over management of any file ending in .bin. Instead of Git tracking the 200MB file directly, LFS will now handle it.**

6. Saved the LFS configuration

   **Executed Git Commands**:

      git add .gitattributes

      git commit -m "setup git lfs"

      **When you run the track command, Git creates or updates a file called .gitattributes. You must commit this file so that anyone else using the repo knows to          use LFS for .bin files.**

7. Added and commit the large file

   **Executed Git Commands**

      git add Sample01.bin

      git commit -m "add large file using lfs"

   **You add the large file just like a normal file. Because of the previous steps, Git will automatically swap the 200MB data for a tiny pointer file during this       commit.**

8. Uploaded to GitHub

   **Executed Git Commands:**

      git push origin lfs
 
**===================================================================================================================================================================**
 
**Q3 Assignment Steps:** 

**1.Start by creating the base branch: geometry-calculator andgeometry_calculator.py with the provided code**

   **Executed Git Commands:**

   git checkout -b geometry-calculator

   # Created geometry_calculator.py with the provided code

   git add geometry_calculator.py

   git commit -m "Initial geometry calculator setup"

**2. Started  on Circle Area:**

   # Edited file geometry_calculator.py: Uncomment the circle code to implent feature/circle-area

**Executed Git Commands:**

   git checkout -b feature/circle-area

   **Apply stash**

   git stash save "Incomplete circle area"

   git status  # Verify working directory is clean

**3. Staretd Working on Rectangle Area :**

   # Editd file  geometry_calculator.py: Uncomment the rectangle code to work on Rectangle feature

   **Executed Git Commands:**

   git checkout -b feature/rectangle-area

   **Aplly stash**

   git stash save "Incomplete rectangle area"

   git status  # Verify working directory is clean

**4. Finished Circle Area Feature:**

   **Executed Git Commands:**

   git checkout feature/circle-area

   git stash list  # Find the index (likely stash@{1})

   git stash apply stash@{0} 

   # Ensure the circle feature is complete/saved

   git add geometry_calculator.py

   git commit -m "Complete circle area implementation"

   git push origin feature/circle-area

**5: Finish Rectangle Area:**

   **Executed Git Commands:**

   git checkout feature/rectangle-area

   git add geometry_calculator.py

   **Apply stash**

   git stash apply stash@{0}

   # Ensured the rectangle feature is complete/saved

   git commit -m "Complete rectangle area implementation"

   git push origin feature/rectangle-area

   **Apply stash** 

   git stash apply 'stash@{0}'

**6: Created Pull request to collaborator**

   feature/circle-area → dev

   feature/rectangle-area → dev
 
 
 
 
   
 
 
 

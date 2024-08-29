#LINKIT GIT WORKSHOP 2024

**Using Git Tags with Semantic Versioning and Branches:**

1. **Initialize Git Repository:**
   ```bash
   git init
   ```

2. **Create Your Project and Commit Initial Code:**
   ```bash
   touch main.sh
   git add main.sh
   git commit -m "Initial commit"
   ```

3. **Create a Major Release (1.0.0):**
   ```bash
   # Create and switch to a branch for the major release
   git checkout -b major-release

   # Make significant changes for the major release
   # Update main.sh and add new features

   git add main.sh
   git commit -m "Add major new features"

   # Create a tag for the major release
   git tag -a 1.0.0 -m "Version 1.0.0"

   # Switch back to the master branch
   git checkout master
   ```

4. **Create a Minor Release (1.1.0):**
   ```bash
   # Create and switch to a branch for the minor release
   git checkout -b minor-release

   # Continue developing and add backward-compatible new features

   git add main.sh
   git commit -m "Add minor new features"

   # Create a tag for the minor release
   git tag -a 1.1.0 -m "Version 1.1.0"

   # Switch back to the master branch
   git checkout master
   ```

5. **Create a Patch Release (1.1.1):**
   ```bash
   # Create and switch to a branch for the patch release
   git checkout -b patch-release

   # Fix a bug in your code

   git add main.sh
   git commit -m "Fix a bug"

   # Create a tag for the patch release
   git tag -a 1.1.1 -m "Version 1.1.1"

   # Switch back to the master branch
   git checkout master
   ```

6. **View Tags:**
   You can view the created tags with the following command:
   ```bash
   git tag
   ```

7. **Merge Branches into Master:**
   To integrate the changes from the major, minor, and patch branches into the master branch, use the following commands:
   ```bash
   git merge major-release
   git merge minor-release
   git merge patch-release
   ```

   Resolve any conflicts that may arise during these merges.

8. **Push Tags and Changes to Remote Repository (if needed):**
   If you have a remote repository, you can push tags and changes to it to make them available to others:
   ```bash
   git push origin --tags
   git push origin master
   ```

Now you've successfully used Git tags with Semantic Versioning in conjunction with branches to manage major, minor, and patch releases in your project. This approach helps maintain a clear versioning scheme while allowing for separate development of different release types.
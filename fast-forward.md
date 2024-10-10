A target branch - a branch to which a merge is made.

In Git, a **fast-forward merge** occurs when the current branch (e.g., `master`) can simply move its pointer to the target branch (e.g., `feature branch`) without any conflicts or need for merging additional commits. This happens when the current branch is a direct ancestor of the target branch.

Before merge to master

![image](https://github.com/user-attachments/assets/f32c9d73-3b58-4cea-a342-30bec41e1084)

After merge to master

![image](https://github.com/user-attachments/assets/419213ef-2900-4208-aca1-4adfddf7e6b4)

Here's an example of how it works:

### Scenario:

1. Your `main` branch is at commit `A`.
2. Your `feature-branch` has one or more commits on top of `A` (e.g., `A -> B -> C`).

If you merge `feature-branch` into `main`, Git can simply "fast-forward" `main` to point to `C`, as `main` doesn't have any commits that `feature-branch` doesn't already have.

### Steps for a Fast-Forward Merge:

1. **Switch to the target branch** (usually `main`):
   ```bash
   git checkout main
   ```

2. **Merge the feature branch**:
   ```bash
   git merge feature-branch
   ```

   If `main` has no new commits since `A`, Git will simply move the pointer to `C`, completing the fast-forward merge.

3. **Push the changes** (if collaborating):
   ```bash
   git push origin main
   ```

### Fast-Forward Merge vs. No Fast-Forward:
- **Fast-Forward** merges don't create a new commit; they simply move the branch pointer.
- **No Fast-Forward** (`--no-ff`) forces a merge commit, even if a fast-forward is possible. This is useful when you want to keep a clear record of merges in the commit history.

   Example of forcing no fast-forward:
   ```bash
   git merge --no-ff feature-branch
   ```

Would you like to know more about any specific scenario?

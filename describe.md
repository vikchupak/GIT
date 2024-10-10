- `git cherry-pick <commit hash>` (multiple or with range, NEW hashes for commits)
- `git merge <branch>` (with squash) | merge commit strategy gitlab. When you use git merge `--squash`, the squashed commit is created in the target branch, not the source branch.
  The --squash option applies the changes from the source branch (or the branch you're merging) into the target branch, but it does not automatically create a merge commit.
  Instead, it stages all the changes as if they were a single commit, and you need to manually commit them.
- `stash`
- `git rm —cached`
- `—no-commit` flag - will reserve auto commit, so we can make additional changes and commit manually later

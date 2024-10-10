- A target branch - a branch to which a merge is made.
- A source branch - a brach which is merged.

In Git, a **fast-forward merge** occurs when the current branch (e.g., `master`) can simply ***move its pointer to the source branch (there will NOT be new commit hashes)*** without any conflicts or need for merging additional commits. This happens when the current branch is a direct ancestor of the source branch.

| Before merge to master | After merge to master |
| ---------------------- | --------------------- |
| <img width="498" alt="01" src="https://github.com/user-attachments/assets/32737aa5-749c-4df6-92c0-250ea17945fc"><img width="498" alt="01" src="https://github.com/user-attachments/assets/f32c9d73-3b58-4cea-a342-30bec41e1084"> | <img width="996" alt="02" src="https://github.com/user-attachments/assets/419213ef-2900-4208-aca1-4adfddf7e6b4"> |

## Fast-forward merge vs No fast-forward
- **Fast-Forward** merges don't create a new commit; they simply move the branch pointer.
- **No Fast-Forward** (`--no-ff`) forces a merge commit, even if a fast-forward is possible. This is useful when you want to keep a clear record of merges in the commit history.

Example of forcing no fast-forward:
```bash
git merge --no-ff feature
```

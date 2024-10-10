`git rebase master` - call when being in a feature branch. The original feature branch with its commits is copied (there will be new commit hashes) on top of the master branch.
The rebased branch can then be merged with fast-forward.

The original branch is not visible, but it is not deleted, and can be accessed via reflog or ORIG_HEAD.
ORIG_HEAD allows to switch only to the most resent original branch, with reflog we can switch to older original branches.
But, it will eventually be garbage collected by Git if it is not referenced by any branches or tags and have been around long enough.
Original branch name and copied branch name are the same.

| Before rebase | After rebase |
| ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| <img width="498" alt="01" src="https://github.com/user-attachments/assets/65fae8e2-c857-4b08-99c3-72028d2d2270"> | <img width="498" alt="02" src="https://github.com/user-attachments/assets/2780d0b8-1593-4230-b699-0f9c3f5068ea"> |
| <img width="498" alt="01" src="https://github.com/user-attachments/assets/0a2dfa29-afef-4a53-a480-dff70cb068f7"> | <img width="498" alt="01" src="https://github.com/user-attachments/assets/c71740a9-6c95-464a-9c2f-11c3676abb03"> |
| <img width="498" alt="01" src="https://github.com/user-attachments/assets/8dc040b6-5c5f-4ab9-9cdc-50ee429c6503"> | <img width="498" alt="01" src="https://github.com/user-attachments/assets/8dc040b6-5c5f-4ab9-9cdc-50ee429c6503"> |

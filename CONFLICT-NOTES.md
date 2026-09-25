# Merge Conflict Resolution Notes

## Cause of the Conflict

Both the `main` branch and the `feature/conflict-demo` branch modified the same section of `README.md` differently. When I merged `main` into `feature/conflict-demo`, Git could not automatically determine which version should be kept, so a merge conflict occurred.

## How I Identified the Conflict

Git reported a content conflict in `README.md`. I used `git status` to identify the conflicted file and inspected the conflict markers in the file.

The conflict markers were:

- `<<<<<<< HEAD`
- `=======`
- `>>>>>>> main`

## How I Resolved It

I reviewed the changes from both branches and decided what the final content should be. I removed the conflict markers, corrected the README content, and saved the file.

I then staged the resolved file to mark the conflict as resolved and created a commit to complete the merge.

## What I Learned

A merge conflict can occur when different branches modify the same part of a file differently. Git identifies the conflicting content, but the developer must decide how the final content should look before completing the merge.
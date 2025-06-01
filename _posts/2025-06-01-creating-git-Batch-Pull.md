## New Blog - Creating Git Batch Pull

Let's test this out. I'm going to toss together a quick project design for a shell script. I will follow up on this project later, and update this blog post.

# Project GithubMassTool

## Goal
- Simplified pulls of multiple github repos at once.
    - This would save me so much time at work doing this manually.

### Acceptance Criteria
For a given folder like so with different github repo clones:
```
    - MainFolder
        - Repo 1
        - Repo 2
        - Repo 3
        - GithubMassPull
```
### Functionality
1. Commands
    1. ***"./GithubMassTool pull"*** command will pull updates from all repos *except* from "GithubMassPull"
    2. ***"./GithubMassTool checkout main"*** command will switch branches for all repos that do not have uncomitted changes *except* from "GithubMassPull"
2. If conflicts arise, the problematic repo is skipped over and output is provided saying as such.
    - Results are also saved in datetimestamped files, for tracability
3. If a username/password or token is required, it will prompt the user to do so at each interval.
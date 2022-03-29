# Refreshing a Fork

*How to Use GitLab*

by j.green

## GitLab Repository Mirror

Navigate into Settings > Repository > Mirroring repositories.

Add the upstream URL

Mirror direction: Pull

Tick Only mirror protected branches (optional)

**This feature is available in the Premium tier: Pull from a remote repository.**

## Git CLI

Add a secondary remote called upstream.
```
git remote add upstream https://...
```
Fetch the remote and then pull its changes into your local default branch, for example main.
```
git checkout main
git fetch upstream
git pull upstream main
```
Last, push to your own remote origin to keep the forked repo in sync.
```
git push origin main
```
Based on the default main branch, you can continue with creating branches, e.g. git checkout -b feature/....

You could also write a script for that, e.g. when you’re syncing between different Git servers.

One liner script in your forked clone:
```
git remote add upstream https://gitlab.com/upstream_user_group/project.git || true && git fetch upstream && git checkout main && git pull upstream main && git push origin main
```

Update the local list of remote branches:
```
git remote update origin --prune
```
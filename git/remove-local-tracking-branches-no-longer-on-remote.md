### Remove local tracking branches no longer on remote

---

This is a small command to remove local branches that no longer exists on remote, found this on [stackoverflow](https://stackoverflow.com/a/33548037)

> The safest way to do this is to use the "plumbing" command git for-each-ref with the interpolation variable %(upstream:track), which will be [gone] when the branch is no longer on the remote:



```bash
git fetch -p && for branch in $(git for-each-ref --format '%(refname) %(upstream:track)' refs/heads | awk '$2 == "[gone]" {sub("refs/heads/", "", $1); print $1}'); do git branch -D $branch; done
```
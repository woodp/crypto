# crypto - Github submodules tests


## Browsing submodules on the web

When the repo has a submodule you will see a special folder that points to the submodule repo. The link is not to master but to a specific commit.


## Cloning
``` 
git clone --recursive <project url>
git clone --recurse-submodules <project url>
```

You need to specify **--recursive** or **--recurse-submodules** to get the submodules, otherwise the folders of submodules will be empty.


## Updating submodules
```
git submodule update --remote
```

Collaborators won’t automatically see updates to submodules — if you update a submodule, you may need to remind your colleagues to run *git submodule update --remote* or they will likely see odd behavior.


## Forking & pull requests
Forking will fork only the parent repo, and leave the submodules at the original user.

A submodule can be forked. When the PR of that fork is merged you need additional steps: 
 - updating the parent repo with *git submodule update --remote*
 - commiting and pushing the changes on the parent repo

Forking the main repo and modifying content on a submodule resulted in strange errors.

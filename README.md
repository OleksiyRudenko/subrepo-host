# Subrepo Hosting Repository

This repo hosts a sub-repo to test git-subrepo workflow

The steps below numbering is consistent across both
[subrepo-host](https://github.com/OleksiyRudenko/subrepo-host)
and [subrepo-repo-b](https://github.com/OleksiyRudenko/subrepo-repo-b)

1) `git checkout -B subrepoB`
2) `git subrepo clone https://github.com/OleksiyRudenko/subrepo-repo-b.git subrepoB -b master`
5) Add changes and `git commit -m "Add intro and STR 1, 2, 5"`
6) Update from `subrepo-repo-B`: `git subrepo pull subrepoB`
7) `git logg` (custom alias)
```
* 64d8269        (HEAD -> subrepoB) git subrepo pull subrepoB
* 9b4e017        Add intro and STR 1, 2, 5
* 3f8c922        git subrepo clone --branch=master https://github.com/OleksiyRudenko/subrepo-repo-b.git subrepoB
* 141aef1        (origin/master, origin/HEAD, subrepo/B, master) Update README.md
* 4919e28        Initial commit
* 0469ab5        (refs/subrepo/subrepoB/pull, refs/subrepo/subrepoB/fetch, refs/subrepo/subrepoB/commit, subrepo/subrepoB) Add STR 4
* 105e204        Add STR
* 13a7b2a        Update README.md
* ef38e97        Initial commit
* bc049d7        (refs/original/refs/heads/subrepoB) git subrepo clone --branch=master https://github.com/OleksiyRudenko/subrepo-repo-b.git subrepoB
```
9) Add changes to main repo and `subrepoB/` (8)
   and `git commit -m "Add STR 6, 7, 8, 9 to the host repo and subrepoB/"`
10) `git subrepo push subrepoB -b patch01`
11) Add changes and `git commit -m "Add STR 10, 11"`
14) `git subrepo pull subrepoB`
15) Add changes and `git commit -m "Add STR 14, 15"`

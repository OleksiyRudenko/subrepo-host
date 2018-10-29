# Subrepo Hosting Repository

This repo hosts a sub-repo to test git-subrepo workflow

See also [Summary](#summary) below

## STR

The steps below numbering is consistent across both
[subrepo-host](https://github.com/OleksiyRudenko/subrepo-host)
and [subrepo-repo-b](https://github.com/OleksiyRudenko/subrepo-repo-b)

(1) `git checkout -B subrepoB`

(2) `git subrepo clone https://github.com/OleksiyRudenko/subrepo-repo-b.git subrepoB -b master`

(5) Add changes and `git commit -m "Add intro and STR 1, 2, 5"`

(6) Update from `subrepo-repo-B`: `git subrepo pull subrepoB`

(7) `git logg` (custom alias)

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

(9) Add changes to main repo and `subrepoB/` (8)
    and `git commit -m "Add STR 6, 7, 8, 9 to the host repo and subrepoB/"`

(10) `git subrepo push subrepoB -b patch01`

(11) Add changes and `git commit -m "Add STR 10, 11"`

(14) `git subrepo pull subrepoB`

(15) Add changes and `git commit -m "Add STR 14, 15"`

(18) `git subrepo push subrepoB -b patch01`

(23) Add changes and `git commit -m "Add STR 23 (host repo only)"`

(24) `git subrepo pull subrepoB`

(25) Add changes and `git commit -m "Add STR 24, 25 (host repo only)"`

(30) `git subrepo push subrepoB -b patch02`

(31) `git logg`
```
 /// skip
```

(32) Add changes and `git commit -m "Add STR 30, 31, 32 (host repo only)"`

(35) `git subrepo pull subrepoB`

(36) `git logg` (custom alias)
```
* f325e38        (HEAD -> subrepoB, origin/subrepoB) Add STR 29 (subrepoB only)
* f64a4e3        Add STR 29 (subrepoB only)
* a6df323        Add STR 28 (subrepoB only)
* ce915a6        Add STR 27 (repoB only)
* 7f9b914        Add STR 26 (repoB only)
* fb2d344        Add STR 24, 25 (host repo only)
* f4df161        git subrepo pull subrepoB
* 39cd777        Add STR 23 (host repo only)
* 5032777        Add STR 17 (subrepoB only)
* ae2bbd6        Add STR 16 (subrepoB only)
* 5ac00a0        Add STR 14, 15 (host only)
* b775ed9        git subrepo pull subrepoB
* bead290        Add STR 10, 11
* e2abf75        Add STR 6, 7, 8, 9 to the host repo and subrepoB/
* 64d8269        git subrepo pull subrepoB
* 9b4e017        Add intro and STR 1, 2, 5
* 3f8c922        git subrepo clone --branch=master https://github.com/OleksiyRudenko/subrepo-repo-b.git subrepoB
* 141aef1        (origin/master, origin/HEAD, subrepo/B, master) Update README.md
* 4919e28        Initial commit
* 3726419        (refs/subrepo/subrepoB/push) Add STR 29 (subrepoB only)
* fb3b8ab        Add STR 28 (subrepoB only)
* 395ce7a        Add STR 27 (repoB only)
* a13cf0b        Add STR 26 (repoB only)
* dfdccbe        (refs/subrepo/subrepoB/pull, refs/subrepo/subrepoB/fetch, refs/subrepo/subrepoB/commit, subrepo/subrepoB) Add STR 22 (repoB only)
* 861a87d        Add STR 21 (repoB only)
* 50a6a94        Add STR 19, 20 (repoB only)
* b612c73        Update README.md
*   517a405      Merge pull request #2 from OleksiyRudenko/patch01
|\
| *   b59c473    Merge branch 'master' into patch01
| |\
| |/
|/|
* | 75842ef      Add STR 13
* |   e138ae0    Merge pull request #1 from OleksiyRudenko/patch01
|\ \
| | * f20cb9e    Add STR 17 (subrepoB only)
| | * 9e8ac2b    Add STR 16 (subrepoB only)
| | * 8fab4d5    git subrepo pull subrepoB
| |/
| * 0ea1f9f      Add STR 6, 7, 8, 9 to the host repo and subrepoB/
|/
* 0469ab5        Add STR 4
* 105e204        Add STR
* 13a7b2a        Update README.md
* ef38e97        Initial commit
* d130aa4        (refs/original/refs/heads/subrepoB) Add STR 29 (subrepoB only)
* c2cdb58        Add STR 28 (subrepoB only)
* fa4717d        Add STR 27 (repoB only)
* 08f5299        Add STR 26 (repoB only)
* 9fe8721        git subrepo pull subrepoB
* a5e987c        Add STR 17 (subrepoB only)
* 71c78cc        Add STR 16 (subrepoB only)
* a245c86        git subrepo pull subrepoB
* 0cd588e        Add STR 6, 7, 8, 9 to the host repo and subrepoB/
* 0689e08        git subrepo pull subrepoB
* bc049d7        git subrepo clone --branch=master https://github.com/OleksiyRudenko/subrepo-repo-b.git subrepoB
```

(37) Add changes and `git commit -m "Add STR 35, 36, 37 (host repo only)"`

## Summary

[subrepo-repo-b](https://github.com/OleksiyRudenko/subrepo-repo-b)
contains commits that
 - were added to `repoB` (`subrepo-repo-b`) directly
 - were added to `host-repo` and touched `subrepoB/`

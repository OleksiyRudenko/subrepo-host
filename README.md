# Subrepo Hosting Repository

This repo hosts a sub-repo to test git-subrepo workflow

The steps below numbering is consistent across both
[subrepo-host](https://github.com/OleksiyRudenko/subrepo-host)
and [subrepo-repo-b](https://github.com/OleksiyRudenko/subrepo-repo-b)

1. `git checkout -B subrepoB`
2. `git subrepo clone https://github.com/OleksiyRudenko/subrepo-repo-b.git subrepoB -b master`
5. Add changes and `git commit -m "Add intro and STR 1, 2, 5"`

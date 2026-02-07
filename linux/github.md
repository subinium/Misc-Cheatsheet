## Github Profile Badge List

- Create a repo with your GitHub username to get a profile README
- Useful badge and profile tools:
  - Badges [shields.io](https://shields.io/)
  - Icons [simpleicons](https://simpleicons.org/)
  - View counter [Hits](https://hits.seeyoufarm.com/)
  - GitHub stats [github-readme-stats](https://github.com/anuraghazra/github-readme-stats)
  - Daily coding [productive-box](https://github.com/maxam2017/productive-box)
  - Pinned Gist [awesome-pinned-gists](https://github.com/matchai/awesome-pinned-gists)
  - BOJ/solved.ac badge [mazassumnida](https://github.com/mazassumnida/mazassumnida)
  - Kaggle badge [kaggle-badge](https://github.com/subinium/kaggle-badge)
  - Code quality [codefactor](https://www.codefactor.io/)
- Official GitHub icons
  - You can use icon links from GitHub Topics [github topics](https://github.com/topics)

## Create and checkout a branch in one step (`git checkout -b` or `git switch -c`)

- Combines these two steps into one:
  - `git branch <branch_name>`
  - `git checkout <branch_name>`

``` sh
git checkout -b <branch_name>

# Modern alternative (Git 2.23+)
git switch -c <branch_name>
```

## Change commit date (`git commit --amend --no-edit --date`)

- Simplest way to change the date of the last commit
- To set it to today, replace the date text with `$(date)`
- Handy for daily commit streaks

```
git commit --amend --no-edit --date "Sat 1 Jan 2022 00:00:00 KST"
```

## Prevent Korean character errors (`core.precomposeunicode`, `core.quotepath`)

- Settings to prevent errors with Korean characters in Git
- Enables Korean input and prevents filename encoding issues

```
git config --global core.precomposeunicode true
git config --global core.quotepath false
```

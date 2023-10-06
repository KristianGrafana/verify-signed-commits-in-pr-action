# Verify Signed Commits in Pull Requests
A GitHub action that can check if commits are signed for all users, or a specific user. 

# How to use

The following action will check that all commits made by user `Octocat` are signed: 
```
name: Verify signed commits in pull requests
on: pull_request

jobs:
  build:
    name: Verify signed commits in pull requests 
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v3
      - name: Verify that all commits made by "octocat" are signed in pull requests 
        uses: KristianGrafana/verify-signed-commits-in-PR@v1
        with:
          user: "octocat"
```

To check all commits, made by any user:
```
      - name: Verify that all commits are signed in pull requests 
        uses: KristianGrafana/verify-signed-commits-in-PR@v1
```

# Demo
Signed PR: https://github.com/KristianGrafana/verify-signed-commits-in-PR-action/pull/1

Unsigned PR: https://github.com/KristianGrafana/verify-signed-commits-in-PR-action/pull/2

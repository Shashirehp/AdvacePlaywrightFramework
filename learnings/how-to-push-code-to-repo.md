# How to push the code into a repository

**Repo:** https://github.com/Shashirehp/AdvacePlaywrightFramework
**Branch:** `main` · **Remote:** `origin`

## Steps

1. **Check where you are.** Confirm the branch and that `origin` points at the right repo.

   ```bash
   git status
   git remote -v
   ```

2. **Stage the files** you want in the commit.

   ```bash
   git add .                  # everything
   git add README.md          # or specific files
   ```

3. **Commit** with a short message.

   ```bash
   git commit -m "your message"
   ```

   If the branch has never been pushed before:

   ```bash
   git push -u origin main    # sets upstream on first push
   ```

   Otherwise:

   ```bash
   git push origin main
   ```

4. **Verify** the remote caught up.

   ```bash
   git fetch origin
   git status -sb             # should show "## main...origin/main" with no ahead/behind
   ```

## Gotchas hit along the way

- **Wrong remote = code goes to the wrong repo.** `git remote -v` first. The remote here is spelled `AdvacePlaywrightFramework` (note: no `n` in "Advace").
- **`git -C "dir" ... ; echo ...` fails on Windows `cmd`.** `;` is not a statement separator there, so chained commands misparse. Run `git -C "dir" <cmd>` on its own, or use `&&`.
- **Heredocs do not work in Windows `cmd`.** `git commit -F - <<'EOF' ... EOF` fails with `<< was unexpected at this time`. Use repeated `-m` flags instead:

  ```bash
  git commit -m "subject" -m "Co-authored-by: Name <email>"
  ```

- **`git mv` into a folder that does not exist yet can fail** with `No such file or directory`. Create the directory first (`mkdir learnings`), then `git mv old new`. `git status` then shows `R  old -> new` (a tracked rename).

## Reusable rule

Before pushing: `git remote -v` and `git status` to know the destination and the state. On Windows, avoid `;` and heredocs — chain with `&&` and pass commit messages with `-m`.

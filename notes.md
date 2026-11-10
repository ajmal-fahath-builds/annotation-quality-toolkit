# Debugging Notes

## Day 1 (Nov 10, 2026): GitHub setup

### The 3 steps to save work (think: sending a box)
1. `git add hello.py` = put the file in the box
2. `git commit -m "Add hello.py"` = seal the box and stick a label on it (saved on my PC only)
3. `git push` = send the box to GitHub (now it shows online)

Always in this order: add, then commit, then push.

### Small things that confused me
- **`git add .`** The `.` means "everything changed in this folder". It needs a space before it because Git reads words separated by spaces: `git` `add` `.`
- **`-m`** means "message". The text in quotes after it is the label for the commit.
- **Why start the label with "Add"?** Just a habit. Labels should say what the commit did (Add, Fix, Update) so old commits are easy to find later.
- **`commit` and `push` have no `.`** because they don't need to be told what to pick. Only `add` does.
- **`--global`** means "save this setting for my whole PC". Setting name and email once with `--global` is enough.
- **Setting vs reading:** with quotes at the end (`git config --global user.name "Ajmal"`) = set it. Without quotes (`git config user.name`) = just show it.

### Errors I hit and what fixed them

**1. "The '<' operator is reserved for future use"**
- Cause: I typed the `<` `>` brackets from the instructions. They were only placeholders.
- Fix: paste the real link with no brackets.
- Also: spaces go between `git`, `clone` and the link. No spaces inside the link.

**2. Repo was inside another project folder**
- Cause: my terminal was already inside PreSynth-Guard when I cloned.
- Lesson: the terminal path (like `C:\Users\Ajmal\...`) shows where I am. Check it before running commands. Use `cd` to move.
- Fix: closed VS Code, cut the folder, pasted it in `C:\Users\Ajmal`, reopened it, ran `git status`.
- The `.git` folder I saw in the old location belonged to PreSynth-Guard. Don't delete it.

**3. "git-credential-manager.exe: The string binding is invalid"**
- Cause: Windows could not save my GitHub login. The login itself worked ("Authentication Succeeded").
- Result: the push still went through. Check for a line like `main -> main` in the terminal.
- If it keeps happening: run `git config --global credential.credentialStore dpapi` and push again.

### Commands I can reuse
- `git status` = what has changed? ("working tree clean" means nothing left to save)
- `python hello.py` = run a Python file (try `py hello.py` if `python` fails)
- `cd folder-name` = move into a folder

### Habit to keep
When I get an error: read it slowly, try for 10 minutes, then ask for help and paste the exact error.

## Still confusing (fill in as I go)
-

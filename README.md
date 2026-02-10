# Mission: SSH Pirates

### Goal

Learn how to connect to a remote computer (the server) using **SSH**, run one simple command, and report back a secret word.

---

## What He'll Learn

* What SSH is (a secure remote connection)
* How to open a terminal on Windows
* How to connect to a server by IP address
* How to type commands carefully
* That computers follow exact instructions

---

## Parent Setup (You do this first)

1. **Create a child account on the server**

   * Example username: `explorer`
   * No sudo/admin permissions

2. **Place a secret file**

   ```bash
   /home/explorer/secret.txt
   ```

   Contents (example):

   ```
   Congratulations! The secret word is DRAGON.
   ```

3. **Make sure SSH is running**

   ```bash
   systemctl status ssh
   ```

4. **Decide authentication**

   * Password is fine for a first lesson **or**
   * SSH key if you already use keys
     (Do not display or store passwords in plain text.)

---

## The Challenge (What He Sees)

### Story Prompt

> A computer far away holds a secret word.
> You must connect to it safely and read the message.
> The server only listens to exact instructions.

---

## Step 1: Open the Terminal (Windows)

Tell him:

1. Press **Windows key**
2. Type **PowerShell**
3. Press **Enter**

Explain:

> This is how we talk to computers using words instead of clicks.

---

## Step 2: Connect to the Server

Give him **only** this instruction (fill in the username you created):

```powershell
ssh explorer@10.10.10.5
```

What to explain:

* `ssh` = secure connection
* `explorer` = his name on the server
* `10.10.10.5` = where the computer lives

If asked about the password:

> Type it carefully. The computer doesn't see letters, only correctness.

---

## Step 3: Look Around

Once connected, give him small "missions":

```bash
ls
```

Explain:

* This means "list what's here"

Then:

```bash
cat secret.txt
```

Explain:

* `cat` means "show me what's inside"

---

## Step 4: Report the Secret

Final task:

> Write down the secret word and tell the Mission Commander (you).

---

## Optional Bonus Challenges

### Level 2 – Navigation

```bash
pwd
```

"What room am I in?"

```bash
whoami
```

"Who am I on this computer?"

---

### Level 3 – Exit Safely

```bash
exit
```

Explain:

> Always leave a computer the same way you entered it.

---

## Teaching Notes (Important)

* Do **not** explain hacking.
* Emphasize:

  * Permission
  * Safety
  * Accuracy
* If he mistypes something, let the error happen and read it together.
* Treat mistakes as clues, not failures.

In GitHub, **"Achievements"** are badges or milestones that recognize your activity and contributions across the platform. These are mostly **fun, motivational, and community-based recognitions**—they don’t affect your code or profile ranking but showcase your engagement.

### 🔥 Common GitHub Achievements

Here are some notable achievements and what you need to do to earn them:

| **Achievement**                      | **How to Earn It**                                                                                                                                    |
| ------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| 🟩 **Arctic Code Vault Contributor** | Have a repository archived in the [GitHub Arctic Code Vault](https://archiveprogram.github.com/arctic-vault/) during the 2020 GitHub Archive Program. |
| 🛡 **GitHub Sponsor**                | Sponsor someone on GitHub or be sponsored.                                                                                                            |
| 🧑‍💻 **Pull Shark**                 | Make a pull request that is merged.                                                                                                                   |
| 🧪 **Galaxy Brain**                  | Answer a discussion that is marked as the accepted answer.                                                                                            |
| 🌱 **First PR**                      | Submit your **first pull request** to any public repo.                                                                                                |
| 🚀 **Pull Blaster**                  | Open **4 or more pull requests** in a **24-hour** period.                                                                                             |
| 💬 **YOLO**                          | Merge your **own** pull request without review (commonly from a repo you own).                                                                        |
| 🔥 **Arctic Vault Contributor-closed!**      | Contributed to a repo archived in the 2020 GitHub Arctic Code Vault.                                                                                  |
| 🧠 **Pair Extraordinaire**           | Co-authored a pull request with another user.                                                                                                         |
| 🕵️ **Quickdraw**                    | Have a pull request merged **within 30 minutes** of opening it.                                                                                       |

---

### 📍 Where to Find Them

* Go to your GitHub profile: `https://github.com/your-username`
* Scroll down to the **"Achievements"** section on your profile (below "Repositories" and "Pinned Repositories")

---

### 🧩 How to Get More Achievements

* Contribute to open-source projects
* Join GitHub discussions
* Create and merge pull requests
* Collaborate with others
* Use GitHub features like **Co-authors**, **Discussions**, **Issues**, and **Sponsorship**

Would you like help unlocking any specific GitHub achievement or improving your profile?


Great! Let's walk through **step-by-step practical examples** to help you earn **GitHub Achievements**, using **dummy projects**. I'll guide you through 5 achievements you can actually earn right now.

---

## 🧪 1. **"First PR" Achievement** done 

> **Goal:** Make your first pull request (PR).

### ✅ Steps:

1. **Fork a public repo**:

   * Go to a simple public repo like [this one](https://github.com/firstcontributions/first-contributions).
   * Click on **“Fork”** (top-right).

2. **Clone your fork**:

   ```bash
   git clone https://github.com/YOUR_USERNAME/first-contributions.git
   cd first-contributions
   ```

3. **Create a branch**:

   ```bash
   git checkout -b add-your-name
   ```

4. **Make a change** (edit a file):

   * Open the repo in VS Code:

     ```bash
     code .
     ```
   * Open `Contributors.md` and add your name like:

     ```
     - Your Name
     ```

5. **Push your changes**:

   ```bash
   git add Contributors.md
   git commit -m "Add my name"
   git push origin add-your-name
   ```

6. **Create a Pull Request (PR)**:

   * Go to your repo on GitHub.
   * Click **“Compare & pull request”**, write a description, and submit it.

🔓 You’ll get the **"First PR"** and **"Pull Shark"** achievements after it’s merged!

---

## 🧠 2. **"Galaxy Brain" Achievement**

> **Goal:** Answer someone’s GitHub **Discussion** and get accepted as the answer.

### ✅ Steps:

1. Go to a repo with **Discussions**, like [microsoft/PowerToys](https://github.com/microsoft/PowerToys/discussions).
2. Find a **“Question”** tagged post and reply with a helpful answer.
3. If the author **accepts your reply**, you get the badge.

💡 Tip: Pick an easy or unanswered topic you know about (e.g., Windows settings, Python tips, etc.).

---

## 🤝 3. **"Pair Extraordinaire" Achievement** DONE

> **Goal:** Co-author a pull request.

### ✅ Steps:

1. Collaborate with a friend or use a second GitHub account.
2. Both contribute to a branch.
3. In your commit message, add:

   ```bash
   git commit -m "Update readme

   Co-authored-by: Another User <their_email@example.com>"
   ```
4. Push and create a PR.

You’ll get the badge after merging the PR with co-authoring.

---

## 💬 4. **"YOLO" Achievement** DONE

> **Goal:** Merge your own PR without review.

### ✅ Steps:

1. Create a **new repo** on GitHub (e.g., `yolo-demo`).

2. Clone and add a dummy file:

   ```bash
   git clone https://github.com/YOUR_USERNAME/yolo-demo.git
   cd yolo-demo
   echo "This is YOLO test" > yolo.txt
   git add .
   git commit -m "Add YOLO test"
   git push origin main
   ```

3. Make a branch, edit something, then push and create a PR:

   ```bash
   git checkout -b update
   echo "Updated YOLO file" >> yolo.txt
   git commit -am "Update YOLO"
   git push origin update
   ```

4. Go to GitHub → create a PR → **merge it yourself** (without review).

Achievement unlocked!

---

## 🚀 5. **"Pull Blaster" Achievement**

> **Goal:** Open 4+ PRs within 24 hours.

### ✅ Steps:

1. Create **dummy repositories**:

   ```bash
   mkdir repo1 repo2 repo3 repo4
   ```

2. Create a file in each and push them to GitHub:

   ```bash
   cd repo1 && git init
   echo "# Test Repo" > README.md
   git add . && git commit -m "init"
   git branch -M main
   gh repo create repo1 --public --source=. --push
   ```

   Do this for all 4 repos.

3. Make a new branch in each, change something small, and create a PR from GitHub.

✅ After opening **4 PRs**, you’ll earn the **Pull Blaster** badge!

---

## 🏁 Summary Table

| **Achievement**     | **Steps**                     |
| ------------------- | ----------------------------- |
| First PR            | Fork + edit file + PR         |
| Pull Shark          | Any merged PR                 |
| Galaxy Brain        | Answer accepted in Discussion |
| Pair Extraordinaire | Co-author commit in PR        |
| YOLO                | Merge your own PR             |
| Pull Blaster        | Open 4+ PRs in 24 hours       |

---


Would you like me to generate a full **starter repo** for one of these steps that you can fork and test?

Absolutely! Let's walk step-by-step through how to earn the **"Pair Extraordinaire" Achievement** on GitHub by co-authoring a pull request.

---

## 🏆 Goal

Create a pull request (PR) that includes a **co-authored commit**, then **merge it**.

---

## 🛠️ Step-by-Step Guide

### ✅ Prerequisites:

* Git and GitHub account set up.
* A **repo** you can contribute to (e.g., your fork of [first-contributions](https://github.com/firstcontributions/first-contributions)).
* You can simulate this with a **second GitHub account**, a friend, or even by faking co-author metadata.

---

### 🔹 Step 1: Fork and Clone the Repository

If not already done:

```bash
git clone https://github.com/your-username/first-contributions.git
cd first-contributions
```

---

### 🔹 Step 2: Create a New Branch

```bash
git checkout -b pair-extraordinaire
```

---

### 🔹 Step 3: Make a Change

Edit a file like `README.md` or `Contributors.md`:

```bash
nano README.md
# or use VS Code
code README.md
```

Add a small line like:

```markdown
This is a test contribution to earn the Pair Extraordinaire badge.
```

---

### 🔹 Step 4: Stage the Change

```bash
git add README.md
```

---

### 🔹 Step 5: Commit with Co-author Info

Use your real email and another email (your alt account or your friend’s):

```bash
git commit -m "Update README to test co-authoring

Co-authored-by: Another User <siddique.bcsir@gmail.com>"
```

Make sure:

* There are **two line breaks** between the title and `Co-authored-by`.
* The co-author email is attached to a valid GitHub account (otherwise, they won't be credited visually).

---

### 🔹 Step 6: Push the Branch

```bash
git push origin pair-extraordinaire
```

---

### 🔹 Step 7: Create a Pull Request

1. Go to your GitHub repo (e.g., [https://github.com/your-username/first-contributions](https://github.com/your-username/first-contributions)).
2. You’ll see a “Compare & Pull Request” button — click it.
3. Add a title and description if needed.
4. Click **Create Pull Request**.

---

### 🔹 Step 8: Merge the Pull Request

Once the PR is created:

1. Scroll down and click **Merge pull request**.
2. Confirm the merge.
3. Delete the branch if prompted (optional).

---

### 🎉 Step 9: Achievement Unlocked

GitHub will detect the `Co-authored-by:` line in the commit and reward both authors. You should see the **"Pair Extraordinaire"** badge on your [GitHub Achievements page](https://github.com/your-username?tab=achievements).

---

### 🧪 Need to Simulate with Yourself?

If you're doing this alone, you can:

* Create a **second GitHub account**.
* Add its email in the `Co-authored-by:` line.
* Or use a **friend’s email** tied to a real GitHub account.

---

Let me know if you'd like a ready-to-use test commit message or help verifying your second GitHub email.

Earning GitHub special achievements like **GitHub Sponsors**, **Arctic Code Vault Contributor**, and **Quickdraw** can be both exciting and valuable for your portfolio. Here's a clear **step-by-step beginner-friendly guide** for each of them:

---

## 🧊 1. **Arctic Code Vault Contributor** (✅ Already closed, but explained)

**🏆 What It Was:**
This badge was given to anyone who contributed code to a public GitHub repository that was part of the **GitHub Arctic Vault** preservation project (2020).

**🎯 Can I Still Get It?**
❌ **No.** This badge was a one-time event. If you contributed to an open-source repo before **Feb 2020**, you may already have it.

**✅ Check if You Got It:**

1. Go to your GitHub profile.
2. Scroll to **“Achievements”**.
3. If you see a **snowflake icon**, you’re an **Arctic Vault Contributor**.

---

## 💸 2. **GitHub Sponsor Achievement**

This badge is for **developers who receive support via GitHub Sponsors**.

### 🪜 Steps to Earn:

#### 🔧 Step 1: **Build a Strong GitHub Profile**

* Upload meaningful, useful, or educational open-source projects.
* Write clear `README.md` files.
* Add licenses (MIT, Apache, etc.).
* Engage with other projects by:

  * Contributing via PRs
  * Reporting issues
  * Writing documentation

#### 📝 Step 2: **Apply to GitHub Sponsors**

1. Go to: [https://github.com/sponsors](https://github.com/sponsors)
2. Click **"Get sponsored"**.
3. Meet these requirements:

   * At least **2FA enabled**
   * Public activity in open-source
   * Complete GitHub profile with:

     * Profile picture
     * Bio
     * Pinned repos
4. Submit the application with details:

   * Why you deserve support
   * What you'll do with the funds

#### 💡 Step 3: **Promote Yourself**

* Share your work on:

  * Twitter / X
  * LinkedIn
  * Developer communities (Reddit, Dev.to)
* Add a **sponsors link** in your GitHub repo and README files.

#### 🔔 When You Get Your First Sponsor:

* You'll get the **GitHub Sponsor badge** on your profile.

---

## 🎯 3. **Quickdraw Achievement**

**🏆 What It Is:**
Awarded to users who complete certain **GitHub Codespaces quickstart** tutorials using **GitHub Codespaces** (cloud-based dev environment).

### 🪜 Steps to Earn:

#### 🔧 Step 1: Enable Codespaces

1. Go to your GitHub profile → **Settings → Codespaces**
2. Make sure it's enabled. You may need to join the [GitHub Codespaces beta](https://github.com/features/codespaces).

#### 🧪 Step 2: Follow the Quickstart Tutorial

GitHub has a tutorial repo:
👉 [https://github.com/githubtraining/quickdraw](https://github.com/githubtraining/quickdraw)

1. Fork the repo.
2. Open the repo in **GitHub Codespaces**.
3. Complete the interactive guide:

   * Run commands in the terminal.
   * Edit files.
   * Commit and push changes.

#### ✅ Step 3: Badge Unlocked!

Once you complete the quickdraw steps, GitHub automatically grants the **Quickdraw** badge.

---

## ✅ Summary Table

| Badge           | How to Earn                                  | Difficulty | Can I Still Earn It? |
| --------------- | -------------------------------------------- | ---------- | -------------------- |
| Arctic Vault    | Contributed to a public repo before Feb 2020 | N/A        | ❌ Closed             |
| GitHub Sponsors | Build open-source projects + get sponsored   | 🔶 Medium  | ✅ Yes                |
| Quickdraw       | Complete GitHub Codespaces tutorial          | 🟢 Easy    | ✅ Yes                |

---

## ✨ Bonus Tips for Beginners

* Start by **contributing to small projects** (fix typos, improve docs, add simple features).
* Use **GitHub Projects** or issues to track your own learning projects.
* Join beginner-friendly open source events:

  * **Hacktoberfest**
  * **EddieHub**
  * **MLH events**

Would you like a **step-by-step GitHub project idea** that helps you work toward the Sponsor badge? I can help you build one!

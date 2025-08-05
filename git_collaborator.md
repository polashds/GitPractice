To allow someone to edit your GitHub repository, you need to **add them as a collaborator** if it's a personal repo, or **give them permissions through a team** if it belongs to a GitHub organization.

---

## ✅ For Personal GitHub Repository

### 🔧 Step-by-step to Add a Collaborator:

1. **Go to your repository** on GitHub.
2. Click on the **"Settings"** tab (⚙️).
3. In the left sidebar, click **"Collaborators"** (or **"Collaborators and teams"**).
4. Click the **"Add people"** button.
5. Enter their **GitHub username or email**.
6. Click **"Add \[username]"**.
7. They will receive an **email invitation** — once they **accept**, they can push/edit code.

---

## ✅ For GitHub Organization Repositories

If the repo is part of an organization:

1. Go to the **organization’s page**.
2. Under **"People"**, add them to a **team**.
3. Give the team **write/admin** access to the repo.
4. Or go to the **repo’s settings > Manage access** and add them directly with specific permission levels.

---

## 🛠️ Permission Levels Explained

* **Read** – Can view the code, issues, and pull requests.
* **Write** – Can push commits, create branches, and open/close issues or PRs.
* **Admin** – Can change repo settings, manage collaborators, delete the repo.

---

## 🔐 Private vs Public Repos

* In **public repos**, anyone can fork but only collaborators can push.
* In **private repos**, only invited collaborators can even see the code.

---

Let me know if:

* You’re using **GitLab**, **Bitbucket**, or something else.
* You want to allow access via **SSH**, **HTTPS**, or **GPG**.
* You want to restrict permissions to certain branches (e.g., via **branch protection**).

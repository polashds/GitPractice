GitHub is rejecting your push because you have files **over the 100 MB hard limit** (`.ipynb` files in this case).

Here’s how you can fix it step-by-step:

---

### **1. Identify the large files**

You already know from the error:

* `image_annotations/scripts/data_annotation_yolov8.ipynb` → **112.67 MB & 104.74 MB** (probably two commits with different versions)
* `torchvision/video_data_exploring.p3.ipynb` → **94.39 MB** (under 100 MB but over GitHub's recommended size of 50 MB)

---

### **2. Remove them from Git history**

Since these files are already **committed**, you must **remove them from the history** or GitHub will still reject the push.

Run:

```bash
# Install BFG (simpler than git filter-branch)
sudo apt install bfg-repo-cleaner  # Linux
# or download from https://rtyley.github.io/bfg-repo-cleaner/

# Backup your repo before doing this
git clone --mirror https://github.com/polashds/image-and-video-processing-opencv-pyhton.git
cd image-and-video-processing-opencv-pyhton.git

# Remove the large files
bfg --delete-files 'data_annotation_yolov8.ipynb'
bfg --delete-files 'video_data_exploring.p3.ipynb'

# Clean and push
git reflog expire --expire=now --all && git gc --prune=now --aggressive
git push --force
```

---

### **3. If you don’t want them in Git but still want to keep them locally**

Instead of committing them, **add to `.gitignore`**:

```gitignore
# Ignore large notebook files
image_annotations/scripts/data_annotation_yolov8.ipynb
torchvision/video_data_exploring.p3.ipynb
```

Then:

```bash
git rm --cached image_annotations/scripts/data_annotation_yolov8.ipynb
git rm --cached torchvision/video_data_exploring.p3.ipynb
git commit -m "Remove large notebooks from Git tracking"
git push
```

---

### **4. If you *do* need to version them**

Use **Git Large File Storage (LFS)**:

```bash
# Install Git LFS
git lfs install

# Track these large files
git lfs track "*.ipynb"

# Add changes to .gitattributes
git add .gitattributes
git add image_annotations/scripts/data_annotation_yolov8.ipynb
git add torchvision/video_data_exploring.p3.ipynb
git commit -m "Track large notebooks with Git LFS"
git push
```

> Note: Git LFS needs to be enabled for your repo on GitHub.

---

If you want, I can **give you the exact `bfg` or `filter-repo` command** for *your* repo so you can clean the history and push without losing your other commits.
Do you want me to prepare that cleanup script for you?


The error is happening because **`git filter-repo` refuses to run on a non-fresh clone** — it’s a safety feature so you don’t accidentally destroy your local repo.

Here’s how you can fix it properly:

---

## **Steps to remove the large files from history and push successfully**

### 1️⃣ Make a fresh clone

Instead of working on your current repo, make a **new clone** into a separate folder:

```bash
cd /e/
git clone https://github.com/polashds/image-and-video-processing-opencv-pyhton.git cleaned-repo
cd cleaned-repo
```

---

### 2️⃣ Run `git filter-repo` to remove both large `.ipynb` files

```bash
git filter-repo --path image_annotations/scripts/data_annotation_yolov8.ipynb --path torchvision/video_data_exploring.p3.ipynb --invert-paths
```

* `--invert-paths` means “keep everything except these files”
* This rewrites the history so those files are **completely gone** from all commits

---

### 3️⃣ Push the cleaned repo (force push)

```bash
git push origin --force --all
git push origin --force --tags
```

> **Warning:** This will overwrite the GitHub history. If anyone else is working on the repo, they’ll need to re-clone it.

---

### 4️⃣ Update `.gitignore` in the cleaned repo so you don’t commit them again

Add these lines:

```gitignore
torchvision/video_data_exploring.p3.ipynb
image_annotations/scripts/data_annotation_yolov8.ipynb
```

---

If you want, I can give you **one combined command** that removes **both large files in one go** from the fresh clone so you don’t have to run `git filter-repo` twice.

Do you want me to prepare that for you? That way the push will work on the first try.


Alright — here’s the **exact full sequence** to completely remove those two large `.ipynb` files from all history and push a clean repo back to GitHub without hitting the 100 MB limit again.

---

## **Final Clean & Push Sequence**

```bash
# 1️⃣ Go somewhere safe (outside your current repo)
cd /e/

# 2️⃣ Clone the GitHub repo into a new folder
git clone https://github.com/polashds/image-and-video-processing-opencv-pyhton.git cleaned-repo

# 3️⃣ Go into the new repo
cd cleaned-repo

# 4️⃣ Remove BOTH large notebooks from the entire history
git filter-repo --path image_annotations/scripts/data_annotation_yolov8.ipynb --path torchvision/video_data_exploring.p3.ipynb --invert-paths

# 5️⃣ Re-add the remote (filter-repo sometimes removes it)
git remote set-url origin https://github.com/polashds/image-and-video-processing-opencv-pyhton.git

# 6️⃣ Force push the cleaned history back to GitHub
git push origin --force --all
git push origin --force --tags
```

---

## **After pushing**

Add the files to `.gitignore` in the cleaned repo so you don’t accidentally re-commit them:

```bash
echo "torchvision/video_data_exploring.p3.ipynb" >> .gitignore
echo "image_annotations/scripts/data_annotation_yolov8.ipynb" >> .gitignore
git add .gitignore
git commit -m "Ignore large notebooks"
git push origin main
```

---

⚠ **Important**
After you do this:

* Your repo history on GitHub will be overwritten (large files gone forever).
* Anyone who has a local clone will need to **delete it and re-clone**.

---

If you want, I can also give you a **smaller variant** that uses just *one single shell command* to run the clone → clean → push sequence in one go. That’s useful if you don’t want to type step-by-step.
Do you want that one-liner version too?

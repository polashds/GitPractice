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

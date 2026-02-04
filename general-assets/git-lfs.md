# Using Git Large File Storage (Git LFS)

Git Large File Storage (LFS) is an extension for Git that helps you manage large files efficiently. Instead of storing large files directly in your Git repository, Git LFS replaces them with lightweight pointer files while keeping the actual content on a separate LFS server.

## Step 1: Install Git LFS

First, install the Git LFS command-line extension on your local machine.

**Installation options:**

* Download and run the installer from the official Git LFS website.
* Use a package manager:

  * macOS: `brew install git-lfs`
  * Windows: `choco install git-lfs`

After installation, open your terminal (or Git Bash) and run:

```bash
git lfs install
```

You only need to do this once per user account or system.

## Step 2: Configure Git LFS in Your Repository

Navigate to the root directory of your Git repository and enable Git LFS:

```bash
cd path/to/your/repo
git lfs install
```

This command adds the required pre-push hook to the repository so Git LFS can manage large files correctly.

## Step 3: Specify Which Files to Track

Use `git lfs track` to tell Git LFS which files or file types to manage. This command creates or updates a `.gitattributes` file in the root of your repository.

**Track all files with a specific extension (example: `.psd`):**

```bash
git lfs track "*.psd"
```

**Track all files in a specific directory (example: `assets/`):**

```bash
git lfs track "assets/*"
```

To see which files are currently tracked by Git LFS:

```bash
git lfs ls-files
```

## Step 4: Commit and Push

Once tracking is configured, follow your normal Git workflow.

**Stage the `.gitattributes` file:**

```bash
git add .gitattributes
```

**Stage your large files:**

```bash
git add path/to/largefile.psd
```

**Commit the changes:**

```bash
git commit -m "Add large file tracking and large files"
```

**Push to the remote repository:**

```bash
git push origin main
```

When pushing, Git LFS uploads the large files to the LFS server and commits only the pointer files to the Git repository.

## Collaborating with Git LFS

* All collaborators must have Git LFS installed on their local machines.
* When users clone the repository, Git automatically downloads the LFS-managed files during checkout if Git LFS is installed.

## Advanced Commands

### Migrate Existing Files

If large files were committed before using Git LFS, you can migrate them:

```bash
git lfs migrate
```

This rewrites repository history. **Always back up your data first.**

### Prune Local Cache

To remove unused LFS files from your local cache and save disk space:

```bash
git lfs prune
```

### File Locking

Git LFS supports file locking to prevent conflicts with binary files that cannot be merged.

* Mark file types as lockable in `.gitattributes`
* Lock a file before editing:

```bash
git lfs lock filename
```


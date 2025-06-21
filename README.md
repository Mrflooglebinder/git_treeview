# Git Tree Viewer

A PowerShell script that displays a graphical directory tree of files and folders tracked by Git in the current branch. The `git_treeview.ps1` script mimics the classic `tree` command but focuses exclusively on Git-tracked items, excluding untracked files, `.gitignore` entries, and build artifacts.

## Features
- Displays a clean, hierarchical view of Git-tracked files and directories.
- Supports custom starting paths within the repository.
- Allows limiting the tree depth with a `MaxDepth` parameter.
- Counts and summarizes directories and files.
- Handles cross-platform path differences (Windows/Linux/Mac).

## Prerequisites
- Git must be installed and accessible in your system's PATH.
- PowerShell 5.1 or later.

## Installation
1. Clone or download the repository:
   ```bash
   git clone https://github.com/your-username/git_treeview.git
   ```
2. Navigate to the repository folder:
   ```bash
   cd git_treeview
   ```
3. Ensure `git_treeview.ps1` is in your working directory.

## Usage
Run the script from a Git repository using PowerShell. Examples:

```powershell
# Show the full Git-tracked tree from the repository root
.\git_treeview.ps1
```

```powershell
# Show the tree starting from a specific folder
.\git_treeview.ps1 -Path .\src
```

```powershell
# Limit the tree to 2 levels deep
.\git_treeview.ps1 -MaxDepth 2
```

## Example Output
```plaintext
.
+-- .gitignore
+-- src
|   +-- main.py
|   L-- utils.py
+-- tests
|   L-- test_main.py
L-- README.md

2 directories, 4 files
```

## Parameters
- `-Path`: Starting path for the tree (default: current directory, `.`).
- `-MaxDepth`: Maximum depth of the tree (default: unlimited).

## Notes
- The script requires a Git repository. Run it from within a repository, or it will error.
- Paths are normalized to ensure compatibility across operating systems.
- The script is read-only and does not modify your repository.

## Contributing
Contributions are welcome! Please:
1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -m 'Add your feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a pull request.

## License
This project is licensed under the GPL-3.0 license. See the [LICENSE](LICENSE) file for details.

## Author
Mrflooglebinder

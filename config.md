# Config levels
- system-wide
- user-specific
- repository-specific

### 1. **System-wide Git Configuration** (`--system`)
This configuration applies to all users and repositories on the system.

- **Location**: This file is usually located at:
  - **Linux/macOS**: `/etc/gitconfig`
  - **Windows**: `C:\Program Files\Git\etc\gitconfig`

To view the configuration, you can run:
```bash
git config --system --list
```
To set system-wide configurations:
```bash
sudo git config --system user.name "Your Name"
sudo git config --system user.email "your.email@example.com"
```

### 2. **User-specific Git Configuration** (`--global`)
This is specific to the user. It applies to all repositories the user works with.

- **Location**: 
  - **Linux/macOS**: `~/.gitconfig` or `~/.config/git/config`
  - **Windows**: `C:\Users\<username>\.gitconfig`

To view the configuration, you can run:
```bash
git config --global --list
```
To set user-specific configurations:
```bash
sudo git config --global user.name "Your Name"
sudo git config --global user.email "your.email@example.com"
```

### 3. **Repository-specific Git Configuration** (`--local`)
This is specific to the current Git repository. It overrides both the global and system-wide configurations.

- **Location**: This file is located inside the `.git` directory of your repository:
  - `path/to/your/repo/.git/config`

To view the configuration, you can run:
```bash
git config --local --list
```
To set repository-specific configurations:
```bash
sudo git config --local user.name "Your Name"
sudo git config --local user.email "your.email@example.com"
```

### Viewing all Configurations:
You can run the following to see all configurations across the different levels (system, global, local):
```bash
git config --list --show-origin
```
This will show you where each configuration setting is coming from.

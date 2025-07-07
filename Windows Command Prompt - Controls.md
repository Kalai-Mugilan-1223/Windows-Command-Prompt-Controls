# Windows Command Prompt Reference Guide

A comprehensive guide to essential Windows CMD commands for file management, application launching, and system operations.

## Table of Contents
- [Environment Variables](#environment-variables)
- [Application Management](#application-management)
- [Package Management](#package-management)
- [Directory Operations](#directory-operations)
- [File Operations](#file-operations)
- [Navigation](#navigation)
- [System Commands](#system-commands)

## Environment Variables

### Setting Environment Variables
Environment variables allow you to create shortcuts to frequently used paths and applications.

#### Temporary Variables (Session Only)
```cmd
set <var_name>="<path>"
```
*Note: No spaces around the equals sign*

#### Permanent Variables (Persistent)
```cmd
setx <var_name> "<path>"
```

**Example:**
```cmd
setx chrome "C:\Program Files\Google\Chrome\Application\chrome.exe"
```

## Application Management

### Launching Applications
#### Open Application with Environment Variable
```cmd
start "" "%<var_name>%"
```

#### Open Chrome with Specific URL
```cmd
start "" "%chrome%" --new-tab <url>
```

#### Open Application from Current Directory
```cmd
<filename.extension>
```

## Package Management

### Windows Package Manager (winget)
#### Search for Packages
```cmd
winget search <package_name>
```

#### Install Packages
```cmd
winget install <package_name>
```

**Example:**
```cmd
winget install Python.Python.3.10
```

## Directory Operations

### Creating Directories
```cmd
mkdir <folder_name>
md <folder_name>
```

### Removing Directories
```cmd
rmdir /s /q <folder_name>
```
*Note: `/s` removes all subdirectories and files, `/q` runs quietly without confirmation*

## File Operations

### Creating Files
```cmd
type nul > <filename.extension>
```
*Note: Always include the file extension*

### Deleting Files
```cmd
del <filename.extension>
```

### Listing Directory Contents
```cmd
dir
```

## Navigation

### Change Directory
#### Direct Path Change
```cmd
cd "<path>"
```

#### Change Drive and Directory Simultaneously
```cmd
cd /d D:\Path\To\Folder
```

#### Navigate to Parent Directory
```cmd
cd..
```

#### Change Drive
```cmd
D:
```

#### View Current Directory
```cmd
cd
```

## System Commands

### Clear Screen
```cmd
cls
```

### Display System Information
```cmd
systeminfo
```

### View Running Processes
```cmd
tasklist
```

## Best Practices

1. **Use Quotes**: Always wrap paths containing spaces in double quotes
2. **Environment Variables**: Use permanent variables (`setx`) for frequently accessed applications
3. **Backup**: Be cautious with delete operations (`del`, `rmdir`) as they may be irreversible
4. **Testing**: Test commands in a safe environment before using them on important files

## Common Examples

```cmd
# Set Chrome as environment variable
setx chrome "C:\Program Files\Google\Chrome\Application\chrome.exe"

# Open Chrome with Google
start "" "%chrome%" --new-tab https://www.google.com

# Navigate to Desktop
cd "%USERPROFILE%\Desktop"

# Create project folder and navigate to it
mkdir MyProject
cd MyProject

# Create a Python file
type nul > main.py

# Install Visual Studio Code
winget install Microsoft.VisualStudioCode
```


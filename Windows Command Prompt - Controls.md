# Windows Command Prompt Reference Guide

A comprehensive guide to essential Windows CMD commands for file management, application launching, system operations, with direct browser access and automation support.

## Table of Contents

* [Environment Variables](#environment-variables)
* [Application Management](#application-management)
* [Package Management](#package-management)
* [Directory Operations](#directory-operations)
* [File Operations](#file-operations)
* [Navigation](#navigation)
* [System Commands](#system-commands)
* [Hotkey Integration](#hotkey-integration)
* [Startup and Script Automation](#startup-and-script-automation)

## Environment Variables

### Temporary Variables (Session Only)

```cmd
set <var_name>="<path>"
```

### Permanent Variables (Persistent)

```cmd
setx <var_name> "<path>"
```

## Application Management

### Launching Browsers Directly

Assuming the browser paths are added to system PATH or set via environment variables:

#### Launch Chrome

```cmd
start chrome "<url>"
```

#### Launch Edge

```cmd
start msedge "<url>"
```

#### Launch Firefox

```cmd
start firefox "<url>"
```

### General Application Launch

```cmd
start "" <application>
```

## Package Management

### Windows Package Manager (winget)

```cmd
winget search <package_name>
winget install <package_name>
```

## Directory Operations

### Creating Directories

```cmd
mkdir <folder_name>
```

### Removing Directories

```cmd
rmdir /s /q <folder_name>
```

## File Operations

### Creating Files

```cmd
type nul > <filename.extension>
```

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

```cmd
cd "<path>"
cd /d D:\Path\To\Folder
cd..
cd
```

### Change Drive

```cmd
D:
```

## System Commands

### Clear Screen

```cmd
cls
```

### Display System Info

```cmd
systeminfo
```

### View Processes

```cmd
tasklist
```

## Hotkey Integration

AutoHotKey Script (`CommandPrompt.exe`) is configured to:

* Open Command Prompt with a specific key combination
* Launch predefined CMD tasks via hotkey mappings

### Script Location

Store the script at:

```plaintext
C:\Scripts\CommandPrompt.exe
```

Ensure the script is registered in startup apps or Task Scheduler for auto-initialization whenever the system restarts.

## Startup and Script Automation

The `bye.bat` file contains:

* Auto-run browser launch commands
* Scripted file or folder setup
* Environment preloading

### Script Location

Store the script at:

```plaintext
C:\Scripts\bye.bat
```

### Integration

* Add `C:\Scripts\bye.bat` to system environment variables for global access:

```cmd
setx bye "C:\Scripts\bye.bat"
```

* Launch via:

```cmd
start "" "%bye%"
```

## Common Usage Examples

```cmd
:: Launch Google in Chrome
start chrome https://www.google.com

:: Navigate to Desktop and setup project
cd "%USERPROFILE%\Desktop"
mkdir MyProject
cd MyProject
type nul > main.py

:: Install Visual Studio Code
winget install Microsoft.VisualStudioCode
```

## Best Practices

1. Always quote paths with spaces
2. Use permanent environment variables for frequently accessed tools
3. Avoid irreversible deletes without confirmation in testing environments
4. Configure scripts in startup for consistent automation

# WSL Recover Files

This directory contains notes and resources for recovering files from WSL (Windows Subsystem for Linux).

## Overview

When working with WSL, you may need to recover files from your Linux distribution or access files stored in the WSL filesystem from Windows.

## File Locations

### Accessing WSL Files from Windows

WSL2 file systems can be accessed from Windows via the network path:
```
\\wsl$\<distro-name>\
```

For example:
```
\\wsl$\Ubuntu\home\username\
```

### WSL File System Location

The WSL file system is typically stored in:
```
%LOCALAPPDATA%\Packages\<WSL_Distro_Package>\LocalState\
```

## Recovery Tips

1. **From Windows Explorer**: Navigate to `\\wsl$\` to access all WSL distributions
2. **From PowerShell/CMD**: Use `\\wsl$\<distro>\` path to access files
3. **Export Distribution**: Use `wsl --export <distro> <filename>` to backup
4. **Import Distribution**: Use `wsl --import <distro> <install-location> <filename>` to restore

## Common Scenarios

- Recovering files after WSL corruption
- Accessing WSL files when the distribution won't start
- Backing up WSL file systems
- Migrating files between WSL instances

## Additional Resources

- [WSL Documentation](https://docs.microsoft.com/en-us/windows/wsl/)
- [WSL File System Support](https://docs.microsoft.com/en-us/windows/wsl/filesystems)

[![Build](https://github.com/uroesch/ApacheDirectoryStudioPortable/workflows/build-package/badge.svg)](https://github.com/uroesch/ApacheDirectoryStudioPortable/actions?query=workflow%3Abuild-package)
[![GitHub release (latest by date including pre-releases)](https://img.shields.io/github/v/release/uroesch/ApacheDirectoryStudioPortable?include_prereleases)](https://github.com/uroesch/ApacheDirectoryStudioPortable/releases)
[![Runs on](https://img.shields.io/badge/runs%20on-Win64%20%26%20Win32-blue)](#runtime-dependencies)
[![Depends on](https://img.shields.io/badge/depends%20on-Java-blue)](#runtime-dependencies)

# Apache Directory Studio Portable for PortableApps.com

<img src="App/AppInfo/appicon_128.png" align=left>

[Apache Directory Studio](https://directory.apache.org/studio/) is a complete 
directory tooling platform intended to be used with any LDAP server however 
it is particularly designed for use with ApacheDS. It is an Eclipse RCP 
application, composed of several Eclipse (OSGi) plugins, that can be easily 
upgraded with additional ones. These plugins can even run within Eclipse itself.

Apache Directory Studio is available for Windows, macOS and Linux.

## Runtime dependencies
* 32-bit or 64-bit version of Windows.
* 32-bit version of Java e.g.
  [OpenJDK JRE](https://portableapps.com/apps/utilities/OpenJDKJRE),
  [OpenJDK](https://portableapps.com/apps/utilities/OpenJDK),
  [JRE](https://portableapps.com/apps/utilities/java_portable) or
  [JDK](https://portableapps.com/apps/utilities/jdkportable) 
  

## Status 
This PortableApp project is in early beta stage. 

## Todo
- [ ] Documentation
- [ ] Download script to fetch the application ZIP file

## Build

### Prerequisites

* [PortableApps.com Launcher](https://portableapps.com/apps/development/portableapps.com_launcher)
* [PortableApps.com Installer](https://portableapps.com/apps/development/portableapps.com_installer)
* [Powershell](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-linux?view=powershell-7)
* [Wine (Linux / MacOS only)](https://www.winehq.org/)

### Build

To build the installer run the following command in the root of the git repository.

```
powershell Other/Update/Update.ps1
```

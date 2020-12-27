[![Build](https://github.com/uroesch/ApacheDirectoryStudioPortable/workflows/build-package/badge.svg)](https://github.com/uroesch/ApacheDirectoryStudioPortable/actions?query=workflow%3Abuild-package)
[![GitHub release (latest by date including pre-releases)](https://img.shields.io/github/v/release/uroesch/ApacheDirectoryStudioPortable?include_prereleases)](https://github.com/uroesch/ApacheDirectoryStudioPortable/releases)
[![Runs on](https://img.shields.io/badge/runs%20on-Win64-blue)](#runtime-dependencies)
[![Depends on](https://img.shields.io/badge/depends%20on-Java-blue)](#runtime-dependencies)
![GitHub All Releases](https://img.shields.io/github/downloads/uroesch/ApacheDirectoryStudioPortable/total?style=flat)

# Apache Directory Studio Portable for PortableApps.com

<img src="App/AppInfo/appicon_128.png" align=left>

[Apache Directory Studio](https://directory.apache.org/studio/) is a complete 
directory tooling platform intended to be used with any LDAP server however 
it is particularly designed for use with ApacheDS. It is an Eclipse RCP 
application, composed of several Eclipse (OSGi) plugins, that can be easily 
upgraded with additional ones. These plugins can even run within Eclipse itself.

Apache Directory Studio is available for Windows, macOS and Linux.

## Runtime dependencies
* 64-bit version of Windows.
* 64-bit version of Java e.g.
  [OpenJDK JRE 64](https://portableapps.com/apps/utilities/OpenJDKJRE64),
  [OpenJDK 64](https://portableapps.com/apps/utilities/OpenJDK64),
  [JRE 64](https://portableapps.com/apps/utilities/java_portable_64) or
  [JDK 64](https://portableapps.com/apps/utilities/jdkportable64) 

## Support matrix

| OS              | 32-bit             | 64-bit              | 
|-----------------|:------------------:|:-------------------:|
| Windows XP      | ![ns][ns]          | ![nd][nd]           | 
| Windows Vista   | ![ns][ns]          | ![ps][ps]           | 
| Windows 7       | ![ns][ns]          | ![ps][ps]           |  
| Windows 8       | ![ns][ns]          | ![ps][ps]           |  
| Windows 10      | ![ns][ns]          | ![fs][fs]           |

Legend: ![ns][ns] not supported;  ![nd][nd] no data; ![ps][ps] supported but not verified; ![fs][fs] verified;

**Note**: With upstream release 2.0.0.v20200411-M15 the ![32bit Windows build has been dropped][32bit-build].
The last release with 32bit support ist [last-32bit][2.0.0.v20180908-M14].

## Status 
This PortableApp project is in beta stage. 

## Todo
- [ ] Documentation

<!-- Start include INSTALL.md -->
## Installation

### Install via the PortableApps.com Platform

After downloading the `.paf.exe` installer navigate to your PortableApps.com Platform
`Apps` Menu &#10102; and select `Install a new app (paf.exe)` &#10103;. 

<img src="Other/Images/install_newapp_menu.png" width="400">

From the dialog choose the previously downloaded `.paf.exe` file. &#10104; 

<img src="Other/Images/install_newapp_dialog.png" width="400">

After a short while the installation dialog will appear. 

<img src="Other/Images/install_newapp_installation.png" width="400">


### Install outside of the PortableApps.com Platform

The Packages found under the release page are not digitally signed so there the installation
is a bit involved.

After downloading the `.paf.exe` installer trying to install may result in a windows defender
warning.

<img src="Other/Images/info_defender-protected.png" width="260">

To unblock the installer and install the application follow the annotated screenshot below.

<img src="Other/Images/howto_unblock-file.png" width="600">

1. Right click on the executable file.
2. Choose `Properties` at the bottom of the menu.
3. Check the unblock box.
<!-- End include INSTALL.md -->

<!-- Start include BUILD.md -->
### Build

#### Windows 10

To build the installer run the following command in the root of the git
repository.

```
powershell -ExecutionPolicy ByPass -File Other/Update/Update.ps1
```

#### Linux (Docker)

Note: This is currently the preferred way of building.

For a Docker build run the following command.

```
curl -sJL https://raw.githubusercontent.com/uroesch/PortableApps/master/scripts/docker-build.sh | bash
```

#### Linux (Wine)

To build the installer under Linux with Wine and PowerShell installed run the
command below.

```
pwsh Other/Update/Update.ps1
```
<!-- End include BUILD.md -->

[nd]: Other/Icons/no_data.svg
[ns]: Other/Icons/no_support.svg
[ps]: Other/Icons/probably_supported.svg
[fs]: Other/Icons/full_support.svg
[32bit-build]: https://github.com/apache/directory-studio/commit/f52d6041fcb3cad0f039903a5c371b1fb8b8d490
[last-32bit]: https://github.com/uroesch/ApacheDirectoryStudioPortable/releases/tag/2.0.0.v20180908-M14-beta3-uroesch

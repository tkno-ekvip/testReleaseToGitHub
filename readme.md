# ekvip, coding ninja monkey base, CNM-Clean-up-assertion-interface-lib

## Table-Of-Contents

1. [Table Of Contents](#table-of-contents)
2. [Abstract](#Abstract)
3. [Folder Structure](#folder-structure)
4. [Branches](#branches)
5. [Version Number Format](#version-number-format)
6. [Contribution](#contribution)
7. [Version Log](#version-log)

## Abstract

* project description: Library provide a collection of assertion interfaces 
* For required software and tools, visit the confluence page:
* [confluence project page](https://ekvip.atlassian.net/wiki/spaces/CNMS/pages/1673527297/CNM_AssertionInterfaceLib)
* [jira project](https://ekvip.atlassian.net/jira/software/projects/CMNB/boards/19?selectedIssue=CMNB-27)
* [bitbucket project page](https://bitbucket.osb-ag.de/projects/CNMTC3/repos/cnm-assertion-interface-lib/browse)

## Folder-Structure

*   **.\\**
*   **build\\** _contains the actual library files (for other test library contains just some unit tests)_
*   **src\\** _root folder for all project sources_
*   **test\\** _root folder project for the unit test project_
*   **.gitignore**  _the git ignore file for this project_
*   **.gitattributes** _the git attribute file for the LFS support_
*   **README.md** _the file you read right now_

## Branches

The repository has some branches to allow collaboration on a centralized repository, and give everybody the possibility to orient onself. We've two main branches, we use this two to branch from and merge to.

> **The Main Branches Are:**
> -   **master**  _here are  **only**  our well tested releases_
> -   **develop**  _this is the choice for new features during the normal project work_

### creating Branches

The initial master commit contains the reworked readme.md, .gitignore and .gitattributes files.
We **only** use the Jira project-tasks (only sub tasks) to create branches. You can choose between **feature** and **hotfix** branches in the Jira menu. To create a branch in Jira, choose the task you want to create a branch for and click on **"Create branch"** at the tab **"Development"** in the task view.

Here are two examples:  **feature/FRINST-14-analogvalueprocessing/efro**  (here is Elias Froschauer working on feature analogvalueprocessing in project FRINST) and  **_hotfix/FRINST-15-analogvalueprocessingbug/toel_**  (here is Tino working on a hotfix for the bug in analog value processing after production release). 

### creating Tags
Every time you finish a task and merge a branch back to the develop or master, then you have to fill out the version log here and you've to tag this commit with the prefix ***"version_"*** and the version number.
If you work in a group and the current online version is not the latest master or develop commit, you will need to tag the currently used branch with **"online"**.

## Version-Number-Format

The version number format for this project has following pattern: ***{major release}.{minor release}.{development state}{maintenance}***. Before the software is deployed to the machine, the major number is zero, if the software is deployed and tested 1st time the major number increase to one.

> **Version Number Format Description:**

> -   **major release**  _marks api changes_
> -   **minor release**  _marks functional extensions or changes but api is still compatible_
> -   **build**  _**odd** number is beta state,  **even**  is stable release
> -   **revision**  _shows the number of patches and hotfixes_

Some examples:

-   **0.0.0.0**  _initial commit_
-   **0.3.0.7**  _add some features and some bug fixes, software is still in alpha state_
-   **0.3.2.9**  _two more bug fixes and the software is now in release state_
-   **1.0.4.15**  _the api has been changed, this needs changes in the used software as well_

## Contribution

-   The language of software and software comments is **English** and software documentation is **English**
-   Use **branch** and **tag** **rules** as defined earlier
-   If you extend or change the folder structure, then you have to **update this file**
-   You have to provide a **version description** with a small change log for every version tag within this file in the version log section
-   If you want to merge you software to the master branch, then you have to take care that your software is compiling  **without warnings and errors**.
-   If you edit this file you've to do it in **English** and to use the **markdown** format
-   It is **not** allowed to work in one of the main branches directly
-   It is **only** allowed to work in your own branches (with your ekvip name acronym)
-   Every commit to feature or hotfix branch needs to contain the **Jira task id** before the commit description

## Version-Log

### Versions 

1.	[0.0.0.0](#0.0.0.0)
2.	[1.2.2.0](#1.2.2.0)
3.	[1.2.2.3](#1.2.2.3)
4.	[3.0.2.1](#3.0.2.1)

### 0.0.0.0 
_initial commit_

### 1.2.2.0
#### **common library information**
*	Build with TwinCAT version 4024.32 **It's compatible from version 4020**
*	Used TwinCAT libraies:
	*	Tc2_Standard 3.3.3.0
	*	Tc2_System 3.4.25.0
	*	Tc2_Utilities 3.3.52.0
*	Used Sytem libraies:
	*	IBaseLibrary 3.5.2.0
	*	SysMem 3.5.12.0
*	Used ekvip libraies:
	*	CNM_AbstractObject 3.5.2.0
	*	CNM_ReturnTypes 3.5.12.0
*	library namespace is *CNM_AssertionInterfaceLib*
*	library placeholder is *CNM_AssertionInterfaceLib*
*	libaray category is ekvip|base|utilities
#### **changes**
* added new to library
	* types
		* subranges
			* `BitNumberByte`
			* `BitNumberDWord`
			* `BitNumberLWord`
			* `BitNumberWord`
			* `BitNumberXWord`
		*	aliases
			* `AssertMessage`
	*	interfaces:
		* `IAssertable`
		* `IAssertCallBack`
		* `IAssertCallBackSetter`
		* `IAssertions`
		* `IBinaryAssertions`
		* `IBitNumberAssertions`
		* `IByteAssertions`
		* `IDwordAssertions`
		* `ILwordAssertions`
		* `IWordAssertions`
		* `IXWordAssertions`
		* `IBooleanAssertion`
		* `I32BitDateAssertions`
		* `I32BitDtAssertions`
		* `I32BitTodAssertions`
		* `IDateAndTimeAssertions`
		* `ISimplyDateAndTimeAssertions`
		* `IFloatAssertions`
		* `ILrealAssertions`
		* `IRealAssertions`
		* `IDintAssertions`
		* `IIntAssertions`
		* `IIntergerAssertions`
		* `ILintAssertions`
		* `ISignedIntegerAssertions`
		* `ISintAssertions`
		* `IUdintAssertions`
		* `IUintAssertions`
		* `IUlintAssertions`
		* `IUnsignedIntegerAssertions`
		* `IUsintAssertions`
		* `IUxintAssertions`
		* `IXintAssertions`
		* `IObjectAssertions`
		* `IPointerAssertions`
		* `IAnyStringAssertions`
		* `IAsciiStringPointerAssertions`
		* `IStringAssertions`
		* `IAsciiStringAssertions`
		* `IUtf16StringAssertions`
		* `IUtf16StringPointerAssertions`
		* `I32BitTimeAssertions`
		* `I64BitTimeAssertions`
		* `ITimeAssertions`
	*	classes:
		* `AbstactAssertion`
		* `AbstractAssertable`
		* `Assertions`
		* `BinaryAssertions`
		* `BitNumberAssertions`
		* `ByteAssertions`
		* `DWordAssertions`
		* `LWordAssertions`
		* `WordAssertions`
		* `XWordAssertions`
		* `BooleanAssertion`
		* `DateAndTimeAssertions`
		* `DateAssertions32Bit`
		* `DateTimeAssertions32Bit`
		* `SimplyDateAndTimeAssertions`
		* `TimeOfDayAssertions32Bit`
		* `FloatAssertions`
		* `LrealAssertions`
		* `RealAssertions`
		* `DintAssertions`
		* `IntAssertions`
		* `IntergerAssertions`
		* `LintAssertions`
		* `SignedIntegerAssertions`
		* `SintAssertions`
		* `UdintAssertions`
		* `UintAssertions`
		* `UlintAssertions`
		* `UnsignedIntegerAssertions`
		* `UsintAssertions`
		* `UxintAssertions`
		* `XintAssertions`
		* `ObjectAssertions`
		* `PointerAssertions`
		* `AbstarctStringPointerAssertions`
		* `AnyStringAssertions`
		* `AsciiStringAssertions`
		* `AsciiStringPointerAssertions`
		* `StringAssertions`
		* `utf16StringAssertions`
		* `Utf16StringPointerAssertions`
		* `SimplyTimeAssertions`
		* `LongTimeAssertions`
		* `TimeAssertions`
	* TwinCAT generated
		*	functions
			*	`F_GetCompany`
			*	`F_GetTitle`
			*	`F_GetVersion`
		*	GVLs
			*	`Global_Version`
* added test project to test the library

### 1.2.2.3
#### **common library information**
*	Build with TwinCAT version 4024.32 **It's compatible from version 4020**
*	Used TwinCAT libraies:
	*	Tc2_Standard 3.3.3.0
	*	Tc2_System 3.4.25.0
	*	Tc2_Utilities 3.3.52.0
*	Used Sytem libraies:
	*	IBaseLibrary 3.5.2.0
	*	SysMem 3.5.12.0
*	Used ekvip libraies:
	*	CNM_AbstractObject 3.5.2.0
	*	CNM_ReturnTypes 3.5.12.0
*	library namespace is *CNM_AssertionInterfaceLib*
*	library placeholder is *CNM_AssertionInterfaceLib*
*	libaray category is ekvip|base|utilities
#### **changes**
*	added null pointer handling to the class `BinaryAssertions`
*	solved spelling errors at the library documentation

### 3.0.2.1
#### **common library information**
*	Build with TwinCAT version 4024.32 **It's compatible from version 4020**
*	Used TwinCAT libraies:
	*	Tc2_Standard 3.3.3.0
	*	Tc2_System 3.4.25.0
	*	Tc2_Utilities 3.3.52.0
*	Used Sytem libraies:
	*	IBaseLibrary 3.5.2.0
	*	SysMem 3.5.12.0
*	Used ekvip libraies:
	*	CNM_AbstractObject 2.0.4.7
	*	CNM_ReturnTypes 4.0.2.0
*	library namespace is *CNM_AssertionInterfaceLib*
*	library placeholder is *CNM_AssertionInterfaceLib*
*	libaray category is ekvip|base|utilities
#### **changes**
*	renamed `AbstractAssertable` to `AbstractAssertor`
*	renamed `simply` properties to `simple`
*	renamed `assertionWasFalse` methods to `assertionWasWrong`
*	solved spelling errors at the library documentation
*	for `BinaryAssertions` and `IBinaryAssertions` changed parameter types from `PVOID` to `ANY`

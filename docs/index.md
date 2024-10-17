# Overview

---

The zOS Rexx Executor can run REXX statements provided in a dataset or in the plugin step.

Apart from executing a REXX program, this plug-in provides ability to create output properties.

## Compatibility

The plug-in is compatible with:

* UrbanCode Deploy version 7.0.0 or later
* UrbanCode Deploy agents on z/OS
* IBM z/OS version 2.1 or later
* IBM Java 8 or 11

## Available Steps

* Execute a REXX program

## Installation

No special steps are required for installation. See [Installing plug-ins in UrbanCode products](https://community.ibm.com/community/user/wasdevops/blogs/laurel-dickson-bull1/2022/06/13/install-plugins).

## History

### Version 2

* Added new checkbox input to show debug logs in case of any unknown failure.
* Output will now show the elapsed time of the REXX program
* New output property RexxReturnCode will store the return code of the REXX program
* Fixes output buffer issue when output has too much data
* Arguments can now be as big as 248 characters
* Fixed issue with work directory during two or more parallel step execution
* Minor improvements in temporary directory creation
* Fixed handling of CLIST error message response from ISPF Gateway
* Changes to run process in Legacy ISPF Gateway
* Improvements in ISPF gateway error handling
* Fixed PH62152 - RcException while allocating temporary datasets

### Version 1

* Initial release
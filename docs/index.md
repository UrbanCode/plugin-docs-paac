# Overview

---

* 'Devops Deploy' processes allows a user to automate a set of repeatable tasks in a orderly fashion and execute them on configured target machines.

* Processes can be configured at 3 places in the product, 'Application', 'Component' , 'Processes' and the processes configured here are termed as 'application process', 'component process', 'generic process' respectively.

* The aim of this project/tool is to allow users to configure their processes in a source code repo like GIT and make it their single source truth and place for users to collaborate to enhance their processes. 

* This tool currently allows users to use json format to define processes and works with existing processes in 'Devops Deploy'.


## History

### Version 2.0
* Added Support to inject the value of a prulin property from a separate file if a user needs. The file path should be prefixed with **scriptFile/** in the respective Json or Yaml files as shown in below Examples:

```json5
"properties": {
        "prop1": "val1",
        "prop2": "scriptFile/PropDetails.txt"
}
```

```
properties:
    prop1: "val1"
    prop2: "scriptFile/PropDetails.txt"
```

### Version 1.2
* Added support to handle Post Processing script's body in separate files during upload and download process. The file path should be prefixed with **scriptFile/** in the respective Json or Yaml files as shown in below examples:

```json5
"postProcessingScript": {
        "name": "MyScript",
        "body": "scriptFile/MyScript.txt"
}
```

```
postProcessingScript:
    name: "MyScript"
    body: "scriptFile/MyScript.txt"
```

#### Disclaimer: The change of the body of a post processing script would affect it globally. It means will be applicable to all the processes in which the post processing script is used.

* Added support for the usage of double-quotes in process step names.

### Version 1.1
* Added support for Yaml files as input/output files along with Json files. Both .yml and .yaml extensions are supported.
* Improved loggings and validations for input parameters of all commands.

### Version 1.0
* Upload commands no longer need process name and the scope(application, component) as arguments and are instead sourced from input file

### Version 0.1.0-Beta

* Initial release
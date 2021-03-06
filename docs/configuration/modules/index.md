---
title: Modules configuration
layout: default
---

The configuration mechanism supports YAML and XML file formats. The framework looks inside all the folders specified
to the [powsybl_config_dirs](../itools.md#powsybl_config_dirs) property in the [itools.conf](../itools.md) file for
configuration files. The framework use the [powsybl_config_name](../itools.md#powsybl_config_name) property as the
basename of the configuration files. It looks for a YAML file first, then for a XML file. The XML file will be used only
if the YAML configuration file has not been found.

The default configuration folder and the configuration file name can be configured in the `POWSYBL_HOME/etc/itools.conf`.

# Modules and properties
The configuration file contains a list of modules, that can be required or optional. Each module contains one or
several properties. These properties can also be required or optional.

## Example

### YAML
```yml
module1:
    property1a: value1
    property1b: value2
    
module2:
    property2a: value3
    property2b: value4
    property2c: value5
```

### XML
```xml
<config>
    <module1>
        <property1a>value1</property1a>
        <property1b>value2</property1b>
    </module1>
    <module1>
        <property2a>value3</property2a>
        <property2b>value4</property2b>
        <property2c>value5</property2c>
    </module1>
</config>
```

# Modules list
- [componentDefaultConfig](componentDefaultConfig.md)
- [computation-local](computation-local.md)
- [default-computation-manager](default-computation-manager.md)
- [external-security-analysis-config](external-security-analysis-config.md)
- [groovy-dsl-contingencies](groovy-dsl-contingencies.md)
- [groovy-post-processor](groovy-post-processor.md)
- [import](import.md)
- [import-export-parameters-default-value](import-export-parameters-default-value.md)
- [javaScriptPostProcessor](javaScriptPostProcessor.md)
- [limit-violation-default-filter](limit-violation-default-filter.md)
- [load-flow-action-simulator](load-flow-action-simulator.md)
- [load-flow-based-phase-shifter-optimizer](load-flow-based-phase-shifter-optimizer.md)
- [load-flow-default-parameters](load-flow-default-parameters.md)
- [loadflow-results-completion-parameters](loadflow-results-completion-parameters.md)
- [loadflow-validation](loadflow-validation.md)
- [local-app-file-system](local-app-file-system.md)
- [mapdb-app-file-system](mapdb-app-file-system.md)
- [remote-service](remote-service.md)
- [security](security.md)
- [simulation-parameters](simulation-parameters.md)
- [table-formatter](table-formatter.md)

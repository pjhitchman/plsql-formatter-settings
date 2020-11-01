# PL/SQL & SQL Formatter Settings

## Introduction

This repository provides formatter settings for the [coding style rules](https://trivadis.github.io/plsql-and-sql-coding-guidelines/v3.6/3-coding-style/coding-style/#rules) of the Trivadis PL/SQL & SQL Coding Guidelines.

Settings are provided for

- [Oracle SQLcl, Version 20.3.0](https://www.oracle.com/tools/downloads/sqlcl-downloads.html)
- [Oracle SQL Developer, Version 20.2.0](https://www.oracle.com/database/technologies/appdev/sql-developer.html) with [patched dbtools-common.jar from SQLcl 20.3.0](https://www.salvis.com/blog/2020/11/01/patching-sql-developer-20-2-with-sqlcls-formatter/)
- [Allround Automations PL/SQL Developer, Version 14.0.3](https://www.allroundautomations.com/products/pl-sql-developer/)

These settings have been defined and tested with the product versions mentioned above. They might not work in other versions.

See [releases](https://github.com/Trivadis/plsql-formatter-settings/releases) for settings supporting older versions.

## Deviating Settings

Please note that these settings do not comply with rule 5. Line breaks are placed after a comma and not before. All other rules are followed. However, you can easily change this in the settings for both products.

## Installation

### Common

Clone this repository or download the ZIP file and extract it. 

### SQL Developer

1. Start SQL Developer
2. Open `Preferences`
3. Select `Code Editor` -> `Format` -> `Advanced Format`
4. Press `Import...`
   ![Advanced Format](images/advanced_format.png)
5. Select [`trivadis_advanced_format.xml`](settings/sql_developer/trivadis_advanced_format.xml)
6. Press `Open`
7. Select `Code Editor` -> `Format` -> `Advanced Format` -> `Custom Format`
8. Press `Import...`
   ![Custom Format](images/custom_format.png)
9. Select [`trivadis_custom_format.arbori`](settings/sql_developer/trivadis_custom_format.arbori)
10. Press `Open`
11. Press `OK` to save the settings

### PL/SQL Developer

1. Start PL/SQL Developer
2. Open `Preferences`
3. Select `User interface` -> `PL/SQL Beautifier`
4. Press `Edit...`
5. Press `Open...`
   ![PL/SQL Beautifier](images/plsql_beautifier.png)
6. Select [`trivadis_beautifier.br`](settings/plsql_developer/trivadis_beautifier.br)
7. Press `Open`
8. Press `Save as...`
9. Select a permanent location for these settings and press `Save` 
10. Press `Close`
11. Select the rule file you've saved previoulsy.
12. Press `OK`

## Arbori

SQL Developer uses its own parse tree query language called Arbori for its advanced formatter configuration. Here is some additional information that might be useful if you plan to tweak the behavior of the formatter yourself.

### Links

- [Formatting Code With SQL Developer](https://www.salvis.com/blog/2020/04/13/formatting-code-with-sql-developer/)
- [SQL Developer 20.2 User Guide, Code Editor: Format](https://docs.oracle.com/en/database/oracle/sql-developer/20.2/rptug/sql-developer-concepts-usage.html#GUID-9421DA6E-A48A-427B-88C9-4414D83EC9D1__GUID-64BE7F6C-37D1-4D21-96A5-E9A19C7D3543)
- [Arbori Starter Manual](https://vadimtropashko.files.wordpress.com/2017/02/arbori-starter-manual.pdf)
- [Semantic Analysis with Arbori](https://vadimtropashko.files.wordpress.com/2019/11/arbori.pdf)
- [Arbori Semantic Actions](https://vadimtropashko.wordpress.com/2019/08/01/arbori-semantic-actions/)
- [Custom Formatting in SQLDev 4.2](https://vadimtropashko.wordpress.com/2017/01/03/custom-formatting-in-sqldev-4-2/)
- [Formula for Formatting](https://vadimtropashko.wordpress.com/2017/09/28/formatting-formulas/) 
- [Custom Syntax Coloring](https://vadimtropashko.wordpress.com/2018/10/10/custom-syntax-coloring/)

Thank you, Vadim Tropashko for providing this valuable information.

### JavaScript Global Variables

To get the most out of the dynamic JavaScript actions from an Arbori program, you should know the following global variables and their corresponding Java class. 

Variable | Type                                             | JAR File
-------- | ------------------------------------------------ | -----------------------
`struct` | oracle.dbtools.app.Format                        | dbtools-common.jar
`target` | oracle.dbtools.parser.Parsed                     | dbtools-common.jar 
`tuple`  | HashMap<String, oracle.dbtools.parser.ParseNode> | dbtools-common.jar
`logger` | oracle.dbtools.util.Logger                       | dbtools-common.jar

## Issues
Please file your bug reports, enhancement requests, questions and other support requests within [Github's issue tracker](https://help.github.com/articles/about-issues/).

* [Questions](https://github.com/Trivadis/plsql-formatter-settings/issues?q=is%3Aissue+label%3Aquestion)
* [Open enhancements](https://github.com/Trivadis/plsql-formatter-settings/issues?q=is%3Aopen+is%3Aissue+label%3Aenhancement)
* [Open bugs](https://github.com/Trivadis/plsql-formatter-settings/issues?q=is%3Aopen+is%3Aissue+label%3Abug)
* [Submit new issue](https://github.com/Trivadis/plsql-formatter-settings/issues/new)

## How to Contribute

1. Describe your idea by [submitting an issue](https://github.com/Trivadis/plsql-formatter-settings/issues/new)
2. [Fork the PL/SQL & SQL Formatter Settings respository](https://github.com/Trivadis/plsql-formatter-settings/fork)
3. [Create a branch](https://help.github.com/articles/creating-and-deleting-branches-within-your-repository/), commit and publish your changes and enhancements
4. [Create a pull request](https://help.github.com/articles/creating-a-pull-request/)

## License

The Trivadis PL/SQL & SQL Formatter Settings are licensed under the Apache License, Version 2.0. You may obtain a copy of the License at <http://www.apache.org/licenses/LICENSE-2.0>.

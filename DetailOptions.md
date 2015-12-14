|-h / --help |help|
|:-----------|:---|
|-r / --show-rules |output the available rules |
|-o output\_file\_name |output file(It's only applied when you assgin --output = csv or xml). If not specified, N'SIQ CppStyle report the output named nsiqcppstyle\_result.XXX in the folder to be analyzed. It's optional. However, if you want analyze multiple folder, It's mandatory.|
|--output= (csv|xml|vs7|emacs) |Output fotmat. csv and xml outputs the result in file form. Rests ouput screen.|
|--no-update  |Do not update automatically |
|-f file\_filter\_file\_location  |location of filefilter.txt|
|--show-url   |When violating rules, report Rule Doc URL|
|--var=key:value,key:value   |Some rule are customizable. You can provide the custom value by this option.|

## How to suppress rule violations ##
  * You may know how to configure filefilter.txt if you alread saw QuickStart.
  * In addition, N'SIQ CppStyle provide the per violation / file violation suppression
  * You can provide the comment just next to the false alarmed violation.
```
ErrorCase // NS
```
  * // NS is short form of No Style. Which means no rules are applied in this line.

  * You can ignore some rules per file. Provide the following line in the first comment of source code.
```
/*
-- RULE_NAME
*/
```
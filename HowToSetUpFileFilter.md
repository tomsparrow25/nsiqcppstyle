## FileFilter ##

If you want to filter in or out some source code files in the target directory please locate filefilter.txt file in the target directory in the form of

```
  * FILTER_SCOPE_NAME
  + INCLUDE_PATH_STRING
  - EXCLUDE_PATH_STRING
  ~ RULE NAME
```


For example, If you provide

```
* default
- \
+ \src\
- \src\test
~ RULES....
```

Above filefilter.txt make nsiqcppstyle analyze all source under \src\ except \src\test\.
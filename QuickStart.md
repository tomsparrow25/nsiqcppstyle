  * It's really simple
### How to set up the rules to be used. ###
  * Make the filefilter.txt in the root folder which contains C/C++ file and write the rules to be used in following way. You can find the lastest available rules in http://nsiqcppstyle.appspot.com/rule_doc/ or just find the rules in the rules folder in N'SIQ CppStyle isntallation.
```
	~ RULE_10_1_A_do_not_use_bufferoverflow_risky_function_for_unix
	~ RULE_10_1_B_do_not_use_bufferoverflow_risky_function_for_windows
	~ RULE_3_1_A_do_not_start_filename_with_underbar
	~ RULE_3_2_B_do_not_use_same_filename_more_than_once
	~ RULE_3_2_CD_do_not_use_special_characters_in_filename
	~ RULE_3_2_F_use_representitive_classname_for_cpp_filename
	~ RULE_3_2_H_do_not_use_underbars_for_cpp_filename
	~ RULE_3_2_H_do_not_use_uppercase_for_c_filename
	~ RULE_3_3_A_start_function_name_with_is_or_has_when_return_bool
	~ RULE_3_3_A_start_function_name_with_lowercase_unix
	~ RULE_3_3_A_start_function_name_with_upperrcase_windows
	~ RULE_3_3_B_start_private_function_name_with_underbar
	~ RULE_4_1_A_A_use_tab_for_indentation
	~ RULE_4_1_A_B_use_space_for_indentation
	~ RULE_4_1_B_indent_each_enum_item_in_enum_block
	~ RULE_4_1_B_locate_each_enum_item_in_seperate_line
	~ RULE_4_1_C_align_long_function_parameter_list
	~ RULE_4_1_E_align_conditions
	~ RULE_4_2_A_A_space_around_operator
	~ RULE_4_2_A_B_space_around_word
	~ RULE_4_4_A_do_not_write_over_120_columns_per_line
	~ RULE_4_5_A_braces_for_function_definition_should_be_located_in_seperate_line
	~ RULE_4_5_A_braces_for_type_definition_should_be_located_in_seperate_line
	~ RULE_4_5_A_braces_inside_of_function_should_be_located_in_end_of_line
	~ RULE_4_5_A_indent_blocks_inside_of_function
	~ RULE_4_5_A_matching_braces_inside_of_function_should_be_located_same_column
	~ RULE_4_5_B_use_braces_even_for_one_statement
	~ RULE_5_2_C_provide_doxygen_class_comment_on_class_def
	~ RULE_5_2_C_provide_doxygen_namespace_comment_on_namespace_def
	~ RULE_5_2_C_provide_doxygen_struct_comment_on_struct_def
	~ RULE_5_3_A_provide_doxygen_function_comment_on_function_in_header
	~ RULE_5_3_A_provide_doxygen_function_comment_on_function_in_impl
	~ RULE_6_1_A_do_not_omit_function_parameter_names
	~ RULE_6_1_E_do_not_use_more_than_5_paramters_in_function
	~ RULE_6_1_G_write_less_than_200_lines_for_function
	~ RULE_6_2_A_do_not_use_system_dependent_type
	~ RULE_6_4_B_initialize_first_item_of_enum
	~ RULE_6_5_B_do_not_use_lowercase_for_macro_constants
	~ RULE_6_5_B_do_not_use_macro_for_constants
	~ RULE_7_1_B_A_do_not_use_double_assignment
	~ RULE_7_1_C_do_not_use_question_keyword
	~ RULE_7_2_B_do_not_use_goto_statement
	~ RULE_8_1_A_provide_file_info_comment
	~ RULE_9_1_A_do_not_use_hardcorded_include_path
	~ RULE_9_2_D_use_reentrant_function
	~ RULE_A_3_avoid_too_deep_blocks
```

  * If you want to rule all available rules first, just run "nsiqcppstyle -r > filefilter.txt".
  * filefilter.txt is configuration file for the friend tool [N'SIQ Collector](http://dev.naver.com/projects/nsiqcollector) originally. This file is used. The filter setting for selecting which file is analyzed by file name pattern matching. N'SIQ CppStyle uses N'SIQCollector filefilter.txt file for reuse the setting. In addition N'SIQ CppStyle uses '~' character to represent the applying rules in filefilter.txt.

  * Some rules above conflict each other. For example, RULE\_4\_1\_A\_A\_use\_tab\_for\_indent and RULE\_4\_1\_A\_B\_use\_space\_for\_indent. So you should carefully pick the appropriate rules which fit your need. .

### How to run  N'SIQ CppStyle on a folder containing C/C++ files ###
  * After rule setting, run following. Of course the folder which stores nsiqcppstyle should be in path.
```
nsiqcppstyle folder_to_be_analyzed
```

  * Then, N'SIQ CppStyle outputs the analyzed result.
```
======================================================================================
Update: checking for update 

============================ Analyzing box ===============================
======================================================================================

 * load rule set in filefilter.txt

  -  RULE_10_1_A_do_not_use_bufferoverflow_risky_function_for_unix is applied. 
    ~~~
  -  RULE_9_1_A_do_not_use_hardcorded_include_path is applied.
======================================================================================

 * report filefilter.txt settings.

Filter Scope "default" is applied.
Current Filter Setting (Following is applied sequentially)
  1. \externals\ is excluded
  2. \box\ is excluded
  3. \tet\ is excluded
  4. \.cvs\ is excluded
  5. \.svn\ is excluded

Current File extension and Language Settings
  C/C++=c,cxx,h,hpp,cpp,hxx

======================================================================================

 * Violation list

d:\sample\a.c(1, 5):  Do not start function name(SetGlobalAuthority) with uppercase  [RULE_3_3_A_start_function_name_with_lowercase_unix] 
d:\sample\a.c(1, 5):  Doxygen Comment should be provided in front of function (SetGlobalAuthority) in impl file.  [RULE_5_3_A_provide_doxygen_function_comment_on_function_in_impl] 
d:\sample\utils\trunk\boxmonlog\boxmonlog.cpp(1, 1):  Please provide file info comment in front of file  [RULE_8_1_A_provide_file_info_comment] 
d:\sample\utils\trunk\boxmonlog\boxmonlog.cpp(21, 6):  Do not start function name(writeLog) with lowercase  [RULE_3_3_A_start_function_name_with_upperrcase_windows] 
d:\sample\utils\trunk\boxmonlog\boxmonlog.cpp(21, 6):  Doxygen Comment should be provided in front of function (writeLog) in impl file.  [RULE_5_3_A_provide_doxygen_function_comment_on_function_in_impl] 
d:\sample\utils\trunk\boxmonlog\boxmonlog.cpp(36, 6):  Do not start function name(openOut) with lowercase  [RULE_3_3_A_start_function_name_with_upperrcase_windows] 
d:\sample\utils\trunk\boxmonlog\boxmonlog.cpp(36, 6):  Doxygen Comment should be provided in front of function (openOut) in impl file.  [RULE_5_3_A_provide_doxygen_function_comment_on_function_in_impl] 
d:\sample\utils\trunk\boxmonlog\boxmonlog.cpp(40, 2):  Matching Braces inside of function should be located in the same column   [RULE_4_5_A_braces_inside_of_function_should_be_located_same_column] 
d:\sample\utils\trunk\boxmonlog\boxmonlog.cpp(44, 3):  Do not use system dependent type(int). Use system independent type like (int32_t)  

============================= Summary Report ==============================

 

 ** Total Available Rules     : 46  
 ** Total Applied Rules       : 43   
 ** Total Violated Rules      : 20   
 ** Total Errors Occurs       : 243  
 ** Total Analyzed Files      : 8    
 ** Total Violated Files Count: 8    
 ** Build Quality             : 0.00%  <== (total analyzed files - the ratio total violated file count) / total analyzed files * 100

=========================== Violated Rule Details ==========================


 -  RULE_4_2_A_A_space_between_operators rule violated : 42
   ~~
 -  RULE_3_3_A_start_function_name_with_is_or_has_when_return_bool rule violated : 11

=========================== Violated File Details ==========================



 -  d:\sample\utils\_service\jobqueue.h  violated in total :  5
   *  RULE_4_2_A_A_space_between_operators  :  1
   ~~
   *  RULE_5_2_C_provide_doxygen_struct_comment_on_struct_def  :  1
 -  d:\sample\utils\_service\broker.cpp  violated in total :  44
   *  RULE_4_2_A_A_space_between_operators  :  10
    ~~
   *  RULE_5_2_C_provide_doxygen_class_comment_on_class_def  :  1

```


### How to run N'SIQ CppStyle on single C/C++ file ###
  * N'SIQ CppStyle supports single file analysis as well as folder analysis. Run following.
```
nsiqcppstyle -f file_filter_file_name file_to_be_analyzed
```
  * When analyzing folder, N'SIQ CppStyle can find the filefilter.txt location under the analyzed folder. However, There is no way to automatically figure out where filefilter.txt is. So you should provide the filefilter file location, when analyzing single file.
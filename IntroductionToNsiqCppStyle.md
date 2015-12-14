N'SIQ CppStyle is the small tool to check C/C++ code against C/C++ coding style.
It's developed to provide the internal free tool in NHN corp, Korea and the source code is opened in http://dev.naver.com/projects/nsiqcppstyle/.

### Feature ###
  * Check more than 47 rules. You can find the available rules in http://nsiqcppstyle.appspot.com
  * No complex preprocess setting(Easy to run. Just run the nsiqcppstyle in the folder to be analyzed.)
  * Rule / Analysis engine separated structure.
    * Easy to add custom rules.
    * Analysis engine parses source code in heuristic way not concrete grammar. So it supports most C/C++ variations.
  * Support IDE integation.
    * Easy to integrate in Visual Studio / Emacs / Eclipse CDT. Support each IDE standard error output format.
  * Support CI server.
    * Support checkstyle xml output. You can use checkstyle plugin in various CI server to show N'SIQ CppStyle result.
  * Various violation suppression
    * It provides 4 way to suppress the false alarm. filefilter / basefile / rule ignore per file / violation ignore
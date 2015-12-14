N'SIQ CppStyle server is developed to support google appengine and django both.
Generic N'SIQ CppStyle server located in http://nsiqcppstyle.appspot.com/

You can use generic N'SIQ CppStyle server or deploy your own server to support custom ruleset.

### How to deploy your own rule server. ###

#### Google AppEngine ####
  1. Please locate nsiqcppstylesvr project in the same folder which containing nsiqcppstyle source.
```
   - nsiqcppstyle_all
     + nsiqcppstylesvr
     + nsiqcppstyle.
```
  1. Get the google appengine account from http://appengine.google.com/
  1. Install Python 2.5
  1. Install google appengine SDK.
  1. Modify the app.yaml file
> > application: nsiqcppstyle ==> application: new google appengine app name.
  1. Run UpdateToAppEngine.bat in nsiqcppstylesvr
> > It will repackage the nsiqcppstyle and unzip it into updatefiles folder.
> > And upload the modified server content into google appengine.
> > You should input the your email and password to upload your rule in the google app engine.

#### Django ####

  1. Install Django.
  1. Please locate nsiqcppstylesvr project in the same folder which containing nsiqcppstyle source.
```
   - nsiqcppstyle_all
     + nsiqcppstylesvr
     + nsiqcppstyle.
```
  1. Run ant update command. It will repackage the nsiqcppstyle and unzip it into updatefiles folder.
  1. Run RunNsiqCppStyleSvrOnDJango.bat for test.
> > test the nsiqcppstylesvr is working well by testing http://localhost:8080
  1. Django server is only working while the current account is loggined. So you should attach apache web server in front.
> > Please refer  http://docs.djangoproject.com/en/dev/howto/deployment/modpython/.

#### How to modify the nsiqcppstyle to connect your own rule server. ####

  * By default, nsiqcppstyle connects the default rule server(http://nsiqcppstyle.appspot.com)
  * However, you can make the nsiqcppstyle connect to new rule server by setting some ant build.xml value.
  * To do it. run ant using following option.
```
   ant package -Dtype=customVersionName -Durl=customRuleServerLocation
```
  * You can get the new version of nsiqcppstyle in the target folder.




**nsiqcppstyle supports checkstyle output. So you can you checkstyle hudson plugin to integrate nsiqcppstyle into hudson.**

**In you build batch file, please add following
```
   nsiqcppstyle --ci --output=xml folder_to_be_analyzed
```**

**or add custom build step**

![http://dev.naver.com/projects/nsiqcppstyle/wiki/Hudson%ED%86%B5%ED%95%A9%EB%B0%A9%EB%B2%95?action=download&value=pic1.png](http://dev.naver.com/projects/nsiqcppstyle/wiki/Hudson%ED%86%B5%ED%95%A9%EB%B0%A9%EB%B2%95?action=download&value=pic1.png)


**You can set nsiqcppstyle\_result.xml file to publish hudson checkstyle output.**

![http://dev.naver.com/projects/nsiqcppstyle/wiki/Hudson%ED%86%B5%ED%95%A9%EB%B0%A9%EB%B2%95?action=download&value=pic2.png](http://dev.naver.com/projects/nsiqcppstyle/wiki/Hudson%ED%86%B5%ED%95%A9%EB%B0%A9%EB%B2%95?action=download&value=pic2.png)
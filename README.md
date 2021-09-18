## 前言

在spring官网偶然发现angular与springboot整合的项目

[Spring Security and Angular](https://spring.io/guides/tutorials/spring-security-and-angular-js/)

觉得非常好可以把前后端分离整合到一个项目里的，发布也可以一块发布，单人开发个项目非常方便，特此记录下

## 准备

首先准备springboot项目与angular项目

具体在[github](https://github.com/dsyer/spring-boot-angular)上

但是这个maven的npm插件版本有点老，版本可以参考本项目的pom文件

## 合并

主要是将angular的项目合并到springboot中

- 将angular中的.gitignore的内容复制粘贴到springboot的.gitignore里

- 然后将angular的所有文件，除了.gitignore和node_modules复制到springboot项目中

- 将angular.json中的outputPath修改为target/classes/static

- 复制本项目中的pom文件的plugins

- maven update project

- run maven genertate-source

- 访问[http://localhost:8080/](http://localhost:8080/)
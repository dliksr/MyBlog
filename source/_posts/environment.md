---
title: 开发环境记录
category:
  - default
tags:
  - blog
sticky: false
copyright: true
comments: true
date: 2021-03-11 08:17:31
---

---

# 前言

记录一下我的开发环境配置

<!-- more -->

# 系统配置

## PowerShell

- 开放第三方脚本运行权限

```shell
set-ExecutionPolicy RemoteSigned
```

# 开发环境

## JDK

- 环境变量

  | 变量名    | 变量值                                                 |
  | --------- | ------------------------------------------------------ |
  | JAVA_HOME | JDK 路径                                               |
  | CLASSPATH | .;%JAVA_HOME%\lib\tools.jar;%JAVA_HOME%\jre\lib\rt.jar |
  | Path      | %JAVA_HOME%\bin                                        |

## NodeJS

- 换源

```shell
npm config -g set registry https://registry.npm.taobao.org
```

- 全局包

```shell
npm install -g @vue/cli hexo-cli http-server
```

## Python

- 换源

```shell
pip config set global.index-url https://mirrors.aliyun.com/pypi/simple
```

## MySQL

- Docker 部署

```shell
docker run --name mysql_5.7 --restart=always --privileged=true -d -p 3306:3306 -v E:/Docker/mysql/conf.d/:/etc/mysql/conf.d/ -v E:/Docker/mysql/data:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=xxxxxx mysql:5.7
```

## Redis

- Docker 部署

```shell
docker run --name redis_6.2 --restart=always --privileged=true -d -p 6379:6379 -v E:/Docker/redis/data:/data -v E:/Docker/redis/redis.conf:/etc/redis/redis.conf redis:6.2 redis-server /etc/redis/redis.conf
```

# 开发工具

## Git

- 配置

```shell
git config --global user.name "dliksr"
git config --global user.email dliksr.kou@gmail.com
git config --global commit.template ~/.gitmessage

git config --global http.proxy http://127.0.0.1:7890
git config --global https.proxy http://127.0.0.1:7890
```

- commit 模板

```
# <类型>[修改范围]: <主题> (最多50个字)

# 解释为什么要做这些改动
# |<----  请限制每行最多72个字   ---->|

# 提供相关文章和其它资源的链接和关键字
# 例如: Github issue #23

# --- 提交 结束 ---
# 主要type
#   feat:     增加新功能
#   fix:      修复bug
# 特殊type
#   docs:     只改动了文档相关的内容
#   style:    不影响代码含义的改动，例如去掉空格、改变缩进、增删分号
#   build:    构造工具的或者外部依赖的改动，例如webpack，npm
#   refactor: 代码重构时使用
#   revert:   执行git revert打印的message
# 暂不使用type
#   test:     添加测试或者修改现有测试
#   perf:     提高性能的改动
#   ci:       与CI（持续集成服务）有关的改动
#   chore:    不修改src或者test的其余修改，例如构建过程或辅助工具的变动
# --------------------
# 注意
#    主题和内容以一个空行分隔
#    主题限制为最大50个字
#    主题行大写
#    主题行结束不用标点
#    主题行使用祈使名
#    内容每行72个字
#    内容用于解释为什么和是什么,而不是怎么做
#    内容多行时以'-'分隔
# --------------------
# 模板更多信息详见下面地址
# https://gist.github.com/adeekshith/cd4c95a064977cdc6c50
# Licence CC
```

## Jetbrains Toolbox

### IDEA

- 注释模板

```java
// Java Class Comments
/*
 * <p>项目名称: ${PROJECT_NAME} </p>
 * <p>文件名称: ${PACKAGE_NAME}.${NAME} </p>
 * <p>创建时间: ${DATE} </p>
 * <p>描述: DOTO </p>
 *
 * @author <a href="mailto:dliksr.kou@gmail.com">dliksr</a>
 * @version v1.0
 */

// Java Method Comments
/**
 * DOTO
 *
 * @Param $param$
 * @Return $return$
 */
```

- VM 参数配置

```
-Dfile.encoding=UTF-8
```

### 第三方插件源

```
https://plugins.zhile.io
https://repo.idechajian.com
```

## Visual Studio Code

- 配置自动同步

## Postman

- 无配置

## Navicat

- 无配置

## Another Redis Desktop Manager

- 无配置

---

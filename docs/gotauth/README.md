# 功能简介

GOT Auth 是一个为专后台系统打造的从粗力度到细粒度完整鉴权系统。既可以用于后台 URI 鉴权，也可以用于控制前端页面展现。

为什么叫 GOT，喜欢冰火的同学肯定知道。Wiki：[冰与火之歌 —— 权力的游戏（A Song of Ice and Fire - Game of Thrones）](https://en.wikipedia.org/wiki/Game_of_Thrones)

在线尝试：

[gotauth-api.felixpy.com](https://gotauth-api.felixpy.com)

仓库地址：

- Service [codetrial/got-auth-service](https://github.com/codetrial/got-auth-service)

后端主要技术：

- Node.js
- Egg.js
- MySQL
- GraphQL

前端主要技术：

- ES6
- React
- Ant Design

## 系统划分

### 应用方

使用鉴权系统的相关系统，下面的资源、角色和分组都必须属于某个应用方。

### 资源

用于描述被鉴权的基本单元，可以被分成多种类型，比如 URI、按钮等。需要注意的是，资源不可以单独分配给用户。

### 角色

一个角色可以包含多个资源，本身也可以单独用于鉴权。可以直接分配给用户。

### 分组

把多个角色聚合为一个分组，从而可以更快的进行授权。本身也可以单独用于鉴权。可以直接分配给用户。

### 用户

业务系统的用户，可以为用户授予分组或角色。
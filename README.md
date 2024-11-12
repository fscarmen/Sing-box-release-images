# Sing-Box 镜像构建
- **使用GitHub Actions自动更新**
- 本教程教您如何使用GitHub Actions 全自动构建Sing-Box Docker镜像

## 当前镜像版本：
 - ### **latest**: v1.10.1
 - ### **dev-next**: v1.11.0-alpha.13

## 教程
### 1. fork仓库

### 2. 查看具体权限
  - 进入fork的仓库后，点击上方 **Settings** ，在左侧菜单中找到**Actions** → **General**，从中找到 **Workflow permissions** 字段，查看是否已经选中 **Read and write permissions** 字段，如未选中，请选中后Save保存，如已选中，则进入下一步

### 3.保存必要字段
  - 点击上方 **Settings** ，在左侧菜单中找到**Secrets and variables** → **Actions**，在**Repository secrets**字段中，点击**New repository secret**，添加如下字段
    - 第一份  
      Name: `DOCKER_REPO`  
      Secret: `Docker Hub的仓库名字，只能用小写字母，尽量避免符号`  

    - 第二份  
      Name: `DOCKER_USERNAME`  
      Secret: `Docker Hub的账号`  

    - 第三份  
      Name: `DOCKER_PASSWORD`  
      Secret: `Docker Hub的密码`  

### 4. 开启编译
  - 点击上方Actions，在左侧找到 **Build latest images**，进入后，在右侧找到**Run workflow**执行

### 至此，全部流程已经已经跑完，稍作等待，当所有流程的前侧变成绿色的对勾后，代表镜像已推送至指定仓库

## 特别感谢  
  - [fscarmen2](https://github.com/fscarmen2/docker_builder)

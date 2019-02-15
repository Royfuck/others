# git配置

### create a new repository on the command line

```bash
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/mazhenting/test.git
git push -u origin master
```

### push an existing repository from the command line

```bash
git remote add origin https://github.com/mazhenting/test.git
git push -u origin master
```

### 为本地与Github的通信配置ssh

本地git仓库与远程git仓库之间的传输是通过SSH加密的，所以：

1. **创建ssh key**: 

```bash
ssh-keygen -t rsa -C "mazhenting44@gmail.com"
```

2. **登陆你的GitHub账号**, `Settings -> SSH and GPG keys -> new SSH key`, 将*C:\Users\mzt\.ssh\id_rsa.pub*的内容复制进去
3. **将本地git仓库push到远程仓库**

```bash
git push -u origin master
```

4. **乱码问题**

```bash
git config --global core.quotepath false
```


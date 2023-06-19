# Chat2CMD

命令行终端GPT对话AI工具，解决运维&开发者遗忘的命令，留在终端里

官方网站：[https://chat2cmd.com](https://chat2cmd.com)

## CHAT2CMD CLIENT GUIDE

**一、直接上⼿**

在shell/cmd等⼯具上，直接使⽤. 在shell/cmd等⼯具的下⼀⾏开始，返回结果，结果⼀般有三类：

- **01.准确结果:**

返回直接可以使⽤的prompt，⽤户回⻋即可执⾏。注：⾮幂等prompt需要⽤户输⼊ y 确认。
```shell
[user@linux ~]# du -h --max-depth=0 //查看当前⽬录使⽤的总空间⼤⼩
```

```shell
[user@linux ~]# mkdir log_dir ? //需要输⼊y才能执⾏命令
```

- **02.建议结果**

返回建议内容，可能包含多个选择，或者需要⽤户⾃⾏选择的结果，不直接产⽣效⽤。

- **03.填空结果**

返回prompt，但其中⼏个变量需要⽤户⾃⾏填写，如 `scp -r {files} {user}@{remote_url}:/{remote_path}`
 

**二、初次登录需要授权**

获取auth_key

在[https://chat2cmd.com](https://chat2cmd.com) 注册之后，可以在任何可联⽹的shell/cmd上使⽤以下命令获取 auth_key :
```shell
[user@linux ~]# cc -u username -p
[chat2cmd:username]password:
```

prompt会提示输⼊隐藏状态的密码。如果验证正确，系统会返回:

```shell
[user@linux ~]#
auth_key(username):1nc889hWc810plx2jhfhaksqwyd73r123jfbuqgca

```


**设置auth_key**

将获得的auth_key进⾏授权设置，可以让⽤户该IP所在的shell/cmd上使⽤chat2cmd时⽆需再进⾏验证。

```shell
[user@linux ~]# cc -a 1nc889hWc810plx2jhfhaksqwyd73r123jfbuqgca
```

也可以在获取auth_key的时候直接授权，如下：

```shell
[user@linux ~]# cc -u username -p -a
[chat2cmd:username]password:
```

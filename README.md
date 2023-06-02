# Typecho_Replit_pgsql

## 修改内容

更改一条代码，避免出现数据库已存在而无法给予权限的问题
增加登录美化和下雪插件
- [LoginDesigner](https://github.com/jrotty/LoginDesigner)
- [Snow-Typecho-Plugin](https://github.com/journey-ad/Snow-Typecho-Plugin)

个人版（不推荐）：
教育版 安装：
<a href="https://repl.it/github/super-yan86/Typecho_Replit_pgsql">
  <img alt="Run on Repl.it" src="https://repl.it/badge/github/super-yan86/Typecho_Replit_pgsql" style="height: 40px; width: 190px;" />
</a></br>
将以下代码粘贴至Replit Shell后回车

```git
git clone https://github.com/Sayafx/Typecho-replit-Pgsql && mv -b Typecho-replit-Pgsql/* ./ && mv -b Typecho-replit-Pgsql/.[^.]* ./ && rm -rf *~ && rm -rf Typecho-replit-Pgsql`
```
当加载完 Loading Nix environment... 后点击绿色 ▶ Run

-----------------------------------------------------------------------------------------------------------------
当clone中出现以下文字时，按说明操作
    初始化完毕
    将文件run.sh第一行的1删去之后再次单击绿色 ▶ Run按钮
    等待小窗口出现后，开始在shell中手动配置数据库
    
-----------------------------------------------------------------------------------------------------------------

在运行完成出现typecho后 点击Shell 在终端中逐行输入以下内容：
```
createdb -h 127.0.0.1
psql -h 127.0.0.1
create user admin with password 'admin';
ALTER DATABASE typecho OWNER TO admin;
GRANT ALL PRIVILEGES ON DATABASE typecho to admin;
```
-----------------------------------------------------------------------------------------------------------------
在新窗口打开你的typecho安装界面
如果新窗口打不开，在小窗口安装
安装好等待片刻就可以在新窗口打开了

选择pgsql原生函数适配器

| 参数 | 值 |
| ---- | ---- |
| 数据库前缀 | typecho_ |
| 数据库地址 | localhost |
| 数据库端口 | 5432 |
| 数据库用户名 | admin |
| 数据库密码 | admin |
| 数据库名 | typecho |

你不用担心数据库密码安全问题，填好各项参数后点击 确认，开始安装 » 设置自己的typecho用户名密码！这个请设置自己的别用弱密码！

sqlite数据库版 + Butterfly主题移植：[https://github.com/super-yan86/Typecho_Replit](https://github.com/super-yan86/Typecho_Replit)</br>
修改自：[https://github.com/valetzx/typechonreplitwithpg](https://github.com/valetzx/typechonreplitwithpg)

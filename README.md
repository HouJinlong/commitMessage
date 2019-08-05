## git 日志规范

> 文章地址 [阮一峰 Commit message 和 Change log 编写指南](http://www.ruanyifeng.com/blog/2016/01/commit_message_change_log.html)


### 1.本地全局使用

[Commitizen](https://github.com/commitizen/cz-cli) 是一个撰写合格 Commit message 的工具。

#### 全局安装 commitizen
```
npm install -g commitizen

```
#### 全局安装 adapter (cz-conventional-changelog/cz-customizable)

> commitizen根据不同的adapter配置commit message。

[cz-conventional-changelog](https://github.com/commitizen/cz-conventional-changelog) (Angular的commit message格式)

```
npm install -g cz-conventional-changelog

```
[cz-customizable](https://github.com/leonardoanalista/cz-customizable) (支持一定程度上的自定义)

```
npm install -g cz-customizable

```
#### .czrc 配置commitizen使用的adapter

当前用户的根目录，新建.czrc

```
echo { "path": "cz-conventional-changelog" } > %USERPROFILE%/.czrc
//echo { "path": "cz-customizable" } > %USERPROFILE%/.czrc

```
> `%USERPROFILE%/`(当前系统用户目录) [window系统下获取当前用户目录](https://www.cnblogs.com/egan123/p/10115639.html)


现在，进入任何git repository, 使用git cz代替git commit提交commit。

![image](http://www.ruanyifeng.com/blogimg/asset/2016/bg2016010605.png)



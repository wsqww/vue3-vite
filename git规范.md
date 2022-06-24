# 悦考云端 git 规范

*version 0.10*



# commit message

## 背景

悦考现在没有一套明确的提交规范, 每个人按照自己的风格和心情写 commit message :如 "fix" "fix some issue"...

这造成代码后续维护成本特别高,合代码时,对每个 commit 的改动内容,需要查看每一个commit 内容才能确定影响范围.耗时且提高了merge风险.

所以参照谷歌的Commit Message Guide 和AngularJS git commit guidelines ,提出以下实现规范.



## 说明

一个完整的 commit message 应该包含三个部分: 

- header
- body
- footer

*示例*

    # header
    feat(dao): add db utils  
    # body
    - describe for util1
    - describe for util2
    see trello 看板卡片
    # footer
    BREAKING CHANGE:...



    <type>(<scope>):<subject>
    <body>
    <footer>



### header

header 只有一行,由三部分组成:

`<type>(<scope>):<subject>`

#### type

说明提交的类别,只允许使用下面的类型.

##### **type可选值**

- feat *新功能(feature)*
- fix *用于修复问题*
- docs *文档*
- style *修改格式(不影响代码运行的变动)*
- refactor *重构*
- perf *优化相关*
- test *增加测试用例*
- revert *回滚*
- merge *合并代码*
- chore *构建过程或辅助工具的变动 如 CI CD*

#### scope(可选)

是可选的,用于说明此次提交影响范围,如数据层,视图层...

由于目前模块化不是很清晰,暂缺省.

#### subject

对提交的简短描述,不超过50字符

**规范**

动词使用第一人称现在时.如 fix 而不是 fixed,add 而不是 added.

首字母小写.

结尾不需要句号.



### body(可选)

body 是可选的,更详细的描述,对于简单的提交也可缺省

*规范*

动词使用第一人称现在时.如 fix 而不是 fixed,add 而不是 added.

用换行分割信息

说明动机和修改前后对比



### footer(可选)

对于不兼容的变更,footer以 `BREAKING CHANGE` 开头.

后面是变动描述,理由等.



### 示例

*vue 项目(同样使用AngularJS规范)里的 git commit message*

    
    feat(reactivity): `proxyRefs` method and `ShallowUnwrapRefs` type (#1682)
    BREAKING CHANGE: template auto ref unwrapping are now applied shallowly,
    i.e. only at the root level. See https://github.com/vuejs/vue-next/pull/1682 for more details.
    

 

    
    fix(hmr): should update el for `HYDRATE_EVENTS` patchFlags node (#1707)
    fix https://github.com/vitejs/vite/issues/613
    

 

    
    refactor(runtime-core): adjust error handling behavior
    - Crash in dev to make the errors more noticeable
    - Recover in prod to reduce impact on end users
    



# git合并和推送流程

todo







# 参考

- [https://www.conventionalcommits.org/en/v1.0.0/](https://www.conventionalcommits.org/en/v1.0.0/)
- [https://developers.google.com/blockly/guides/modify/contribute/commits](https://developers.google.com/blockly/guides/modify/contribute/commits)
- [https://github.com/angular/angular.js/blob/master/DEVELOPERS.md#-git-commit-guidelines](https://github.com/angular/angular.js/blob/master/DEVELOPERS.md#-git-commit-guidelines)




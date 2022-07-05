# git 规范
# commit message

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

- feat **增加新功能**
- bug **测试反馈bug列表中的bug号**
- fix **修复bug**
- ui **更新UI**
- docs **文档变更**
- style **代码格式(不影响代码运行的变动)**
- perf **性能优化**
- refactor **重构(既不是增加feature，也不是修复bug)**
- release **发布**
- deploy **部署**
- test **增加测试**
- chore **构建过程或辅助工具的变动(更改配置文件)**
- revert **回退**
- build **打包**

#### scope(可选)

可选, 用于说明此次提交影响范围

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


# 项目使用的辅助插件及配置说明

### husky
```

```

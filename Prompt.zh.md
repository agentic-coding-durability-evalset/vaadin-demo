## 任务1

**任务类型：** 需求实现

**提示词：**
```
需要实现一个Snippet功能，主要是保存snippet，主要包括title, filename, code, tags等信息。

- 新增Snippet Entity类
- 新增Snippet Repository类
- 新增Snippet Service类
- 新建SnippetListView，主要用于展现snippet，包括增加新snippet，修改snippet，删除snippet，搜索snippet
- 将新增SnippetListView添加到MenuBar 中

请借鉴Task的实现代码，完成Snippet的实现。
```


## 任务2

**任务类型：** 需求实现

**提示词：**
```
请为Task类添加tags字段，tags是一个逗号分隔的字符串，如`vip,paid`。
添加tags字段后，请修改TaskListView类，添加tags字段的输入框，并实现搜索功能。
```

## 任务3

**任务类型：** 需求实现

**提示词：**
```
为Vaadin应用添加登录支持，只有登录后才能访问该应用，要求如下：

- 创建对应的account表，包括username, email, roles, password等字段，其中密码采用bcrypt加密算法，角色包括ADMIN和USER
- account相关的代码，请放置在`org.mvnsearch.account` package下
- 为account表添加默认数据，如user和admin账号
- 添加顶部导航栏，在右侧显示登录后的用户头像和用户名，同时增加退出登录按钮
```

## 任务4

**任务类型：** 需求实现

**提示词：**

```
请根据excalidraw文件中的钱包原型图，创建对应的Vaadin View，包括消费记录添加操作。
```
## 本项目实现的最终作用是基于SSH个人博客管理系统
## 分为1个角色
### 第1个角色为用户角色，实现了如下功能：
 - 个性化设置
 - 博客首页
 - 添加文章
 - 用户注册
 - 用户登陆
 - 相册设置
## 数据库设计如下：
# 数据库设计文档

**数据库名：** ssh_blog_person

**文档版本：** 


| 表名                  | 说明       |
| :---: | :---: |
| [article](#article) | 文章表 |
| [bloginfo](#bloginfo) | 个性设置表 |
| [critique](#critique) | 评论表 |
| [dianjiliang](#dianjiliang) | 点击量表 |
| [user](#user) | 用户表 |

**表名：** <a id="article">article</a>

**说明：** 文章表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | title |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 标题  |
|  3   | content |   text   | 65535 |   0    |    Y     |  N   |   NULL    | 内容  |
|  4   | username |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 用户名  |
|  5   | date |   datetime   | 19 |   0    |    Y     |  N   |   NULL    | 日期  |
|  6   | hasread |   int   | 10 |   0    |    Y     |  N   |   0    |   |

**表名：** <a id="bloginfo">bloginfo</a>

**说明：** 个性设置表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | username |   varchar   | 255 |   0    |    N     |  Y   |   ''    | 日期  |
|  2   | blogtitle |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  3   | idiograph |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="critique">critique</a>

**说明：** 评论表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | AId |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |
|  3   | content |   text   | 65535 |   0    |    Y     |  N   |   NULL    | 内容  |
|  4   | username |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 用户名  |

**表名：** <a id="dianjiliang">dianjiliang</a>

**说明：** 点击量表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | AId |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |
|  3   | ip |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | IP地址  |
|  4   | time |   date   | 10 |   0    |    Y     |  N   |   NULL    | 时间日期  |

**表名：** <a id="user">user</a>

**说明：** 用户表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | username |   varchar   | 255 |   0    |    N     |  Y   |   ''    | 日期  |
|  2   | password |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 密码  |
|  3   | nickname |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 昵称  |
|  4   | question |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  5   | answer |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 答案  |


## 本项目实现的最终作用是基于JSP在线学生信息管理系统
## 分为1个角色
### 第1个角色为管理员角色，实现了如下功能：
 - 修改密码
 - 学生信息管理
 - 年级信息管理
 - 数据字典类别维护
 - 数据字典维护
 - 班级信息管理
 - 管理员登录
## 数据库设计如下：
# 数据库设计文档

**数据库名：** stuinfosys

**文档版本：** 


| 表名                  | 说明       |
| :---: | :---: |
| [t_class](#t_class) |  |
| [t_datadic](#t_datadic) |  |
| [t_datadictype](#t_datadictype) |  |
| [t_grade](#t_grade) |  |
| [t_student](#t_student) | 学生信息表 |
| [t_user](#t_user) | 用户表 |

**表名：** <a id="t_class">t_class</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | classId |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | className |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  3   | gradeid |   int   | 10 |   0    |    Y     |  N   |   NULL    | 年级ID  |
|  4   | classDesc |   text   | 65535 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="t_datadic">t_datadic</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | ddId |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | ddTypeId |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |
|  3   | ddValue |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  4   | ddDesc |   text   | 65535 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="t_datadictype">t_datadictype</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | ddTypeId |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | ddTypeName |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  3   | ddTypeDesc |   text   | 65535 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="t_grade">t_grade</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | gradeId |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | gradeName |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  3   | gradeDesc |   text   | 65535 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="t_student">t_student</a>

**说明：** 学生信息表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | studentId |   varchar   | 255 |   0    |    N     |  Y   |       | 学生ID  |
|  2   | stuNo |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  3   | stuName |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  4   | stuSex |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  5   | stuBirthday |   date   | 10 |   0    |    Y     |  N   |   NULL    |   |
|  6   | stuRxsj |   date   | 10 |   0    |    Y     |  N   |   NULL    |   |
|  7   | stuNation |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  8   | stuZzmm |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  9   | classId |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |
|  10   | stuDesc |   text   | 65535 |   0    |    Y     |  N   |   NULL    |   |
|  11   | stuPic |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="t_user">t_user</a>

**说明：** 用户表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | UserId |   int   | 10 |   0    |    N     |  Y   |       | 用户ID  |
|  2   | userName |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 用户名  |
|  3   | password |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 密码  |

**运行不出来可以微信 javape 我的公众号：源码码头**

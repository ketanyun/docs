# Official Docs for Quantangle Cloud 

# CRD 定义 
* 所有CRD均需限定命名空间 

| Name | Multitenancy | Explained | 
|------|------|-----|
| [QApp](../../wiki/QApp) | `Yes` | OAuth应用 | 
| [QService](../../wiki/QService) | `Yes` | 服务注册 |
| [QRole](../../wiki/QRole) | `No` | 描述ACL |
| [QCanvas](../../wiki/QCanvas) | `Yes` | 数据应用 |
| [QWorkflow](../../wiki/QWorkflow) | `Yes` | 流程应用 |
| [QForm](../../wiki/QForm) | `Yes` | 表单界面定义，被数据应用、流程应用等所引用 |
| [QChart](../../wiki/QChart) | `Yes` | 图表定义，被数据应用引用 |
| [QSurvey](../../wiki/QSurvey) | `Yes` | 问卷定义 |
| [QPatch](../../wiki/QPatch) | `?` | 应用补丁 |
| [QLicense](../../wiki/QLicense) | `No` | 应用授权|
| [QDataSource](../../wiki/QDataSource) | `yes` | 数据源定义 |
| [QUserSource](../../wiki/QUserSource) | `yes` | 身份权威源定义 |


# CRD 设计原则 
## 一致原则
* 当有些属性符合如下语义时，使用相同语法：
  * `name` : 人编的唯一机读编码，导入导出不变，数组内唯一，以方便Patch定位 
  * `text` ：人读的短描述，用于显示
  * `description` ：人读的长描述
  * `uri` ：全剧资源定位符，用于外部资源定位/链接 
  * `tags` ： 标签，用于分类、索引 

## 简化原则
* boolean类型，不使用is开头，直接后面的形容词
* 如多个属性需要拥有相同前缀，考虑提取公共对象，层级下移
  * 比如 { fieldName, fieldType}  应使用 { field { name, type } }
* 在避免关键字冲突的前提下简化。这包括但不限于：
  * OpenAPI Schema 关键字：`items`、`type`、`properties`，避免解析问题
  * 编程语言关键字：`int`、`var`、`for` 等，避免序列化问题 

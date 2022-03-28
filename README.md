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

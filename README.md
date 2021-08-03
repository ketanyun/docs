# Official Docs for Quantangle Cloud 

# CRD 定义 
* 所有CRD均需限定命名空间 

| Name | Multitenancy | Explained | 
|------|------|-----|
| [QApp](#QApp) | `Yes` | OAuth应用 | 
| [QService](QService) | `Yes` | 服务注册 |
| [QRole](QRole) | `No` | 描述ACL |
| [QCanvas](QCanvas) | `Yes` | 数据应用 |
| [QWorkflow](QWorkflow) | `Yes` | 流程应用 |
| [QForm](QForm) | `Yes` | 表单界面定义，被数据应用、流程应用等所引用 |
| [QPatch](QPatch) | `?` | 应用补丁 |
| [QLicense](QLicense) | `No` | 应用授权|
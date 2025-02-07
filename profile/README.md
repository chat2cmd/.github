# TorchV 

当前分组是[TorchV](https://www.torchv.com)的核心代码仓库，项目包括产品、项目等模块 



## 产品

目前主要产品包含两个：

- TorchV AI：大模型基础底座应用平台
- TorchV KB：大模型知识库协作平台

源码项目说明：

|项目名称|地址|说明|
|-------|-------|------|
|torchv ai|[https://github.com/chat2cmd/torchv_server](https://github.com/chat2cmd/torchv_server)|该项目的master分支是当前生产环境最新代码|
|torchv kb|[https://github.com/chat2cmd/torchv_server](https://github.com/chat2cmd/torchv_server)|该项目的dev-kb分支是当前测试环境最新代码|
|reranker|[https://github.com/chat2cmd/torchv_reranker](https://github.com/chat2cmd/torchv_reranker)|RAG技术服务重排序的模型接口封装|
|embedding|[https://github.com/chat2cmd/torchv_embedding](https://github.com/chat2cmd/torchv_embedding)|文本向量模型的API接口封装|
|pipeline|[https://github.com/chat2cmd/torchv_pipeline](https://github.com/chat2cmd/torchv_pipeline)|TorchV AI\TorchV KB底层数据支撑接口，依赖Python得生态，提供包括语义分词、数据转换处理等接口的封装|

## 项目

主要包含的项目：

- 国科云招数字AI名片：基于员工数字名片+RAG问答构建的一套面向政府招商的系统项目

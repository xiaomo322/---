# 智库管理助手
## 项目概述
智库管理助手是基于自然语言处理与数据分析的数据服务系统，面向数据仓库的应用场景，旨在用户通过对话，高效获取数据仓库中的数据，对于自然语言的问题进行仓库数据的理解，计算分析，以及可视化

## 快速开始

### 环境要求
python 3.12


### 安装依赖
  1.项目需要的全部基础服务通过Docker Compose统一部署  
  
  进入docker-compise.yaml所在的目录执行以下命令： 
  
  docker compose up -d  
  

  2.在项目命令行执行安装项目所需要的依赖
  当然一步步的学习可以遇到再装这里提前装了


*uv add fastapi[standard] sqlalchemy asyncmy qdrant-client "elasticsearch[async]>=8,<9" langchain langchain-huggingface langgraph jieba omegaconf pyyaml loguru cryptography langchain-deepseek*  
### 配置文件
在python终端执行一下命令脚本  

python -m app.scripts.build_meta_knowledge -c .\conf\meta_config.yaml   
### 启动服务
在终端执行  
fastapi dev
### 启动前端项目
准备好node环境后  

在agent-fronted根目录下执行  
npm install
nom run dev

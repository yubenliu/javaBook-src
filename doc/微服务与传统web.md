# 微服务
- Author: [HuiFer](https://github.com/huifer)
## 传统 web 开发
### 特点
1. 功能都在一个包中
1. 没有外部依赖
1. 部署在一个 servlet 容器中

### 优势
1. 集中式管理
1. 基本不会重复开发
1. 功能在本地,不需要进行分布式管理
### 劣势
1. 开发效率低
1. 代码维护成本高
1. 部署时间长
1. 稳定性不高
1. 拓展性不够

## 微服务开发
### 特点
1. 多个独立服务组成一个完整的系统
1. 独立部署
1. 服务之间独立开发业务
1. 分布式管理
1. 按照业务划分服务
### 优势
1. 开发简单
1. 技术选择灵活
1. 可用性高
1. 按需求拓展业务
### 劣势
1. 多个服务的运维难度
    - 单体架构只需要保证一个项目正常运行,微服务项目中需要保证多个正常运行
1. 系统集成
1. 测试
    - 各个服务自身的 junit 测试
    - Pair 集成测试
    - Contract 集成测试
    - 契约测试
        - 金字塔理论: https://martinfowler.com/bliki/TestPyramid.html
        - Integration Tests Are a Scam : http://blog.thecodewhisperer.com/permalink/integrated-tests-are-a-scam
1. 接口调整成本高
    - 服务A修改了接口,其他调用者也需要同步修改
1. 服务间通讯
    - RPC \ REST
1. 性能监控
1. 拆分服务的难度
    - 单一职责
    - 界定业务范围
1. 数据一致性
    - sagas 模式
1. 公共代码的开发
    - 多个服务存在相同功能,该功能没有达到可以拆分微服务的程度.一般会使用公共库来解决,但是多语言环境下公共库似乎不是那么优秀.
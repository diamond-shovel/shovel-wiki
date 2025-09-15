# 节点(Slave)是什么

节点是任务运行的工作单元。每个节点都可以运行一个或多个任务。节点可以是物理服务器、虚拟机或容器等。

节点的基础参数包括:

| 属性 | 描述 | 类型 |
|---|---|---|
| service_type | 节点的服务类型，0为远程服务，1为Docker服务，2为本地服务 | int |
| access_point | 节点的访问点，0时为URL，1时为Docker的端点::容器ID，2时不用填 | Optional[str] |

## 节点的部署和注册

请参考[diamond-shovel](https://github.com/diamond-shovel/diamond-shovel)中的部署方法，即
```bash
pip install diamond-shovel
diamond-shovel -I
diamond-shovel -D
```

部署后请对应的在`shovel-intermediate-layer`中配置节点的访问点(`access_point`)和服务类型(`service_type`)以连接。


# Fabric2.0 Java Sdk Demo
1. 该项目提供了fabric2.0的java sdk的使用案例，仅供参考
2. FabricManager类是操作管理工具类，用它就好了
3. 需要自己修改init中的证书、私钥和域名，FabricManager中也有一个方法中需要改
4. 安装链码需要项目目录中有src目录，链码文件在src下，安装时只需提供项目目录即可。2.0的安装流程是 打包->安装->审批->提交，每个组织的锚节点都得安装，每个组织都得审批通过，后面才能执行链码。因为我的通道的默认背书策略是每个组织的Admin都有参与。
5. 注释还行吧，应该自己能看懂，记得安装go、java和Fabric环境。
## 目录
* chaincode目录中是链码安装和调用的方法，如客户端初始化，链码安装、审批、提交，调用。
* channel目录中是通道安装和加入节点的方法
* fabcar目录中是官方的链码示例，用来安装
* po目录中是一些实例对象，用于返回值，后台请求等
* rKey目录中是证书和私钥
* script目录中是一些配置网络环境的自动化脚本
* Fabric配置.txt中是命令行配置环境的命令
* FabricManager类是工具类的入口文件，用它就好了
## 功能
1. 安装链码（可以自动下载链码需要的依赖，安装成功后自动删除链码和依赖文件）
2. 初始化链码
3. 执行链码
4. 查询链码
5. 获取节点加入的所有通道
6. 获取节点安装的所有链码
7. 创建通道，加入节点
## maven
```
<dependencies>
  <dependency>
    <groupId>com.alibaba</groupId>
    <artifactId>fastjson</artifactId>
    <version>1.2.75</version>
  </dependency>
  <dependency>
    <groupId>org.hyperledger.fabric-sdk-java</groupId>
    <artifactId>fabric-sdk-java</artifactId>
    <version>2.0.0</version>
  </dependency>
</dependencies>
```

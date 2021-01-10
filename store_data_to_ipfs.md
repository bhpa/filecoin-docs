#### 							如何将应用程序数据存储在IPFS上

**1.构建IPFS 节点或集群**

​	安装IPFS节点，参照：

https://docs.ipfs.io/install/command-line/#package-managers

​	初始化IPFS节点

https://docs.ipfs.io/how-to/command-line-quick-start/#prerequisites

​	自定义IPFS节点配置

https://docs.ipfs.io/how-to/configure-node/

​	NAT 配置

https://docs.ipfs.io/how-to/nat-configuration/

​	默认配置文件

https://docs.ipfs.io/how-to/default-profile/

​	自定义IPFS 节点存储库（若未自定义，则在初始化IPFS 节点时在默认位置创建存储库）

​	使用 IPFS Repo自定义IPFS存储库，例子：

https://github.com/ipfs/js-ipfs/tree/master/examples/custom-ipfs-repo

​	IPFS Repo 说明文档。

https://github.com/ipfs/js-ipfs-repo#setup

​	另：构建IPFS 集群

https://docs.ipfs.io/install/server-infrastructure/#create-a-local-cluster

**2.使用 IPFS API 存储、读取、下载数据**

举例：

通过命令行添加文件到IPFS 存储库

ipfs add -q test.txt | tail -n1

返回 一个 hash

查看文件 ipfs cat hash



​	IPFS 命令行，参照

https://docs.ipfs.io/reference/cli/#ipfs

​	IPFS HTTP API reference  参照：

https://docs.ipfs.io/reference/http/api/

**说明：每一个可用的cli 命令都对应一个 api 接口，应用程序通过访问API 接口可查看，下载文件**

**3，IPFS Companion** 

https://docs.ipfs.io/how-to/command-line-quick-start/#ipfs-companion

功能及说明：

https://github.com/ipfs-shipyard/ipfs-companion#features



**4.其他**

其他版本IPFS节点及功能

https://docs.ipfs.io/install/ipfs-desktop/


**5.crust apps**
app :   https://github.com/polkadot-js/apps
explorer : https://apps.crust.network/#/explorer
web apps：https://github.com/crustio/crust-apps

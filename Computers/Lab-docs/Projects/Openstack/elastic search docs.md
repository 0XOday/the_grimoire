installation 

HW req - 
## [Memory](https://www.elastic.co/docs/deploy-manage/deploy/cloud-enterprise/ece-hardware-prereq#ece-memory)

| **Memory**             | Coordinators | Directors  | Proxies   | Allocators            |
| ---------------------- | ------------ | ---------- | --------- | --------------------- |
| Minimum to install     | 8 GB RAM     | 8 GB RAM   | 8 GB RAM  | 8 GB RAM              |
| Minimum recommended    | 16 GB RAM    | 8 GB RAM   | 8 GB RAM  | 128 GB to 256 GB RAM1 |
| **Small deployment**2  | 32 GB RAM    | 32 GB RAM  | 16 GB RAM | 128 GB RAM            |
| **Medium deployment**2 | 32 GB RAM    | 32 GB RAM  | 16 GB RAM | 256 GB RAM            |
| **Large deployment**3  | 128 GB RAM   | 128 GB RAM | 16 GB RAM | 256 GB RAM            |

## [Storage](https://www.elastic.co/docs/deploy-manage/deploy/cloud-enterprise/ece-hardware-prereq#ece-storage)

|**Storage**|Coordinators|Directors|Proxies|Allocators|
|---|---|---|---|---|
|Minimum to install|10 GB|10 GB|15 GB|10 GB|
|Minimum recommended|1:4 RAM-to-storage ratio1|1:4 RAM-to-storage ratio1|1:4 RAM-to-storage ratio1|Enough storage to support the RAM-to-storage ratio2|

software pre-req

## [XFS](https://www.elastic.co/docs/deploy-manage/deploy/cloud-enterprise/ece-software-prereq#ece-xfs)

XFS is required if you want to use disk space quotas for Elasticsearch data directories.

Disk space quotas set a limit on the amount of disk space an Elasticsearch cluster node can use. Currently, quotas are calculated by a static ratio of 1:32, which means that for every 1 GB of RAM a cluster is given, a cluster node is allowed to consume 32 GB of disk space.

XFS and quotas enabled on all allocators to display disk usage correctly.  

system rec 
 [Disabled nscd daemon](https://www.elastic.co/docs/deploy-manage/deploy/cloud-enterprise/ece-sysconfig#ece-sysconfig-nscd)
	 On Linux systems, the [name service cache daemon (nscd)](https://linux.die.net/man/8/nscd) can prevent ECE from installing successfully. For example, it might block various networking components from functioning properly, including the container’s ability to resolve connections to its host. Before running the ECE install process this service should be disabled on your system. The nscd daemon needs to be permanently stopped, even after ECE installation.

https://www.elastic.co/docs/deploy-manage/deploy/self-managed/important-system-configuration

![[Pasted image 20250507151822.png]]


## [Directory layout of RPM](https://www.elastic.co/docs/deploy-manage/deploy/self-managed/install-elasticsearch-with-rpm#rpm-layout)

The RPM places config files, logs, and the data directory in the appropriate locations for an RPM-based system:

|Type|Description|Default Location|Setting|
|---|---|---|---|
|home|Elasticsearch home directory or `$ES_HOME`|`/usr/share/elasticsearch`||
|bin|Binary scripts including `elasticsearch` to start a node and `elasticsearch-plugin` to install plugins|`/usr/share/elasticsearch/bin`||
|conf|Configuration files including `elasticsearch.yml`|`/etc/elasticsearch`|[`ES_PATH_CONF`](https://www.elastic.co/docs/deploy-manage/deploy/self-managed/configure-elasticsearch#config-files-location)|
|conf|Environment variables including heap size, file descriptors.|`/etc/sysconfig/elasticsearch`||
|conf|Generated TLS keys and certificates for the transport and http layer.|`/etc/elasticsearch/certs`||
|data|The location of the data files of each index / shard allocated on the node.|`/var/lib/elasticsearch`|[`path.data`](https://www.elastic.co/docs/deploy-manage/deploy/self-managed/important-settings-configuration#path-settings)|
|jdk|The bundled Java Development Kit used to run Elasticsearch. Can be overridden by setting the `ES_JAVA_HOME` environment variable in `/etc/sysconfig/elasticsearch`.|`/usr/share/elasticsearch/jdk`||
|logs|Log files location.|`/var/log/elasticsearch`|[`path.logs`](https://www.elastic.co/docs/deploy-manage/deploy/self-managed/important-settings-configuration#path-settings)|
|plugins|Plugin files location. Each plugin will be contained in a subdirectory.|`/usr/share/elasticsearch/plugins`||
|repo|Shared file system repository locations. Can hold multiple locations. A file system repository can be placed in to any subdirectory of any directory specified here.|Not configured|[`path.repo`](https://www.elastic.co/docs/deploy-manage/tools/snapshot-and-restore/shared-file-system-repository)|
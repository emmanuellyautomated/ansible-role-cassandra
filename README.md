
## ansible role for cassie
Ansible role for cassandra

### Usage

The variables required for this role are:

|  Name          | Default Value                 | Description   |
|----------------|-------------------------------|---------------|
|new_jvm_heap_size| 800M                         | jvm heap size when it starts up|
|max_jvm_heap_size| 4G                           | Max size for the jvm |
|cluster_name     | Dev Cluster                  | used for logical grouping of cassandra nodes|
|seed_nodes       | 127.0.0.1                    | Seeds for the new nodes to connect |
|listen_address   | 127.0.0.1                    | Address for the cassandra node to listen on|
|rpc_address      | 127.0.0.1                    | Set for accessing cassandra node outside of the cassandra cluster|
|broadcast_rpc_address| 127.0.0.1                | Can be set to the same value as rpc_address|
|endpoint_snitch | SimpleSnitch                  | Snitch for cassandra|
|cassandra_version | dsc-cassandra-3.0.9 | Cassandra version to install|
|cassanra_url     | http://downloads.datastax.com/community/{{ cassandra_version }}-bin.tar.gz | Url to fetch cassandra installation|


You could set variable values for specific hosts in the inventory file

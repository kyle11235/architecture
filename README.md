# architecture

- science/todo/share + communication

- HA

        HA LB (master slave) + HA stateless apps (active active) + shared file storage HA + DB HA (master slave)
        
        - LB layer                                

                - F5
                - cloud LB
                - LVS vs Nginx

        - middleware layer
        
                - memcache cluster（full replicate）
                - redis sharding (sharding + slave) 
                - solrcloud sharding (sharding + redundant replicas)

        - storage layer / shared storage
        https://blog.csdn.net/ds1130071727/article/details/80395551
                
                - NAS (network attached system)
                is file system, e.g. NFS, simple yet scalability bottleneck
                HA = NFS + inotify (monitor file event) + rsync (remote file sync) + keepaliaved (monitor server failure based on LVS)

                - cluster storage 
                is file system, e.g. GFS, HDFS

                - SAN （Storage Area Network）
                non file system, for Oracle RAC, extensiable, fast network, quick backup

        - DB layer

                - oracle RAC, ADG

- security/access

        - jenkins
        - weblogic
        - springsecurity
        - k8s security

- scalability
- API/integration
- monitoring/log & matric
